# TL;DR

From the creator of serverless. To solve a new problem of event driven systems, event driven gateways -> CloudEvents


# Resources
https://github.com/cloudevents/spec
https://twitter.com/clemensv/status/992478395178119168
> At the core, CloudEvents is an "envelope" format. The full event data is carried inside "data" and there are various attributes that describe the event so that it can be generically tracked, routed, and dispatched by infrastructure.

> For those who recall, one of the grand "envelope" standards efforts was SOAP. I'm just going to call that out before anyone else does 😀 While it remains in widespread enterprise use even for new development today, SOAP ultimately lost the "SOAP/REST wars". What went wrong?

> 1. SOAP made a hard bet on elements and attributes (XML). That ended up being a terrible fit for a world of arrays and maps and values (everything else)
> 2. SOAP and WS-* treat all transports as dumb pipes and then tried to reinvent everything from IP+TCP to TLS at the SOAP level
> 3. In spite of being usable for one-way flows, SOAP and WS-* mostly assume that there's a request/response relationship between parties. SOAPAction is the RPC giveaway, because it telegraphs "DO THIS" rather than humbly declaring the message type and letting the recipient decide.

> In CloudEvents we might make new mistakes, but we'll not make these mistakes again if I can help it 😀
> First, CloudEvents envelopes are one-way letters. If people want to create complex flows on top (including request/response) that's great and the metadata should allow that.
> Events just declare what they contain; they carry facts. They are not saying "do this!" indicating what to do with the event - because that is the slippery slope to having feedback requirements (leading to RPC). Receivers autonomously decide on what to do with the events.
> Liberated from any inherent request/response smell, you now have a model that allows one-way distribution, pub/sub with many subscribers, and storage in logs (even cryptographically signed ones if you want)
> Second, CloudEvents has its own minimal abstract type system just sufficient for the defined metadata attributes: String, Binary, URI, Map, Object (variant). Those map into encodings via event formats. We started with JSON, but I can see BSON, MessagePack, Avro, AMQP .. (XML? 😬)
> Related: The event payload can either use the encoding of the event format for the envelope, or can have a completely different one. You should be able to carry the binary legacy format of an existing plant-floor device unchanged.
> Third, I try hard to invent nothing. So far, the CloudEvents transport mappings largely just constrain existing protocols (HTTP is partially in v0.1, AMQP, MQTT, and HTTP WebHooks are in PRs) aiming to map the event into the respective protocol as appropriate for that protocol.
> The MQTT mapping projects events onto the 3.1.1 and 5.0 PUBLISH package using the appropriate facilities the respective version provides. The AMQP mapping projects events onto the AMQP message. Neither spec dictates how to handle or dispatch events. 100% interop focus.
> Security is a point in all those specs: "This specification does not introduce any new security features for MQTT, or mandate specific existing features to be used" - which is to say "inventing the grand unifying security theory is not the point here; use what exists"
> Summary: From the Microsoft perspective, we're trying to help making a set of specs that fit into ecosystems rather than require their own ecosystem - and that are nevertheless composable.
> An event dropped via HTTP should be routable via AMQP to an MQTT subscriber - and yet the event mapping onto those transports should feel "normal" and work with all existing tooling you've got and the encodings you use now.

https://serverless.com/event-gateway/
https://medium.com/@austencollins/introducing-cloudevents-a758c62c76bf

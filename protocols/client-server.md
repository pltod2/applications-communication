# List with possible approaches

Here the approaches are kind of mixed.

We have more **technical aspect of the communication (e.g. AJAX)** and **architecture aspect of communication (e.g. SPA, SSR)**.


* Server Generated JavaScript Templates (SJR)

* Server Sent Events

* Streaming chunked HTML

* AJAX

* Polling, Long polling, WebSockets - These are kind of streams

* Duplex streams like Socket.io

* Mixed mode of SPA + SSR

> Points of SSR sent to client

> And then we go with SPA as we could leverage either 1) SJR (partial SSR) or 2) Pure AJAX call for getting JSON data

* RESS looks similar to SJR but considers the user agent to sent appropriate for the device markup

# Summary

What we have is the following:

* How the markup is served - in respect to rendering

* How the code and styles are served - in respect to loading

* How the data is served - in respect to polling, long polling, streaming

Note that this is essential document for the following reasons:

* knowing this explains why different architectural approaches appear

* knowing this explains why different framewoks appear



## Serving HTML

### Static Page

* html is generated in advanced and served by static server together with the corresponding resources


### Dynamic Page - Server Side Rendering

* html is generated on demand by a client with server side templates

* this is what 37 signals call it SGR (and could be done with react)

* however here nothing is said about how the the SSR DOM has active event handlers

* in the case of CM app I was doing it with attaching flight components to DOM


### Dynamic Page - Mixed Rendering

* html is generated on client demand partially with server side templates

* additional rendering is made on the client with client side templates

* this in my oppinion is very rare


### Dynamic Page - Client Side Rendering

* html is generated on client demand

* html skelethon is served statically and additional rendering is made on the client

* client side rendering was popular in early AMD projects.

> It was insired by the possibilty of having SPA apps

> But basically it introduced problems like the lack of SEO, reusability, performance on mobiles (which ISOMORPHIC architectures were trying to solve later)


## Serving Code and Styles (JS and CSS)

The latest trends towards serving code is on component base. 
Which means when we need particular component to appear on screen we download the corresponding code, markup and styles.


### download all js at once

### download asynchronously on demand

* this will reduce the size of the artifacts but it will increase the http requests in case we touch functionality that needs not loaded js



## Serving Data


### Waiting for all

* in SSR the application waits for getting the data so it renders the data together with the html and then serve it

### Waiting for none

* the application just send the rendered html template

* data is collected with AJAX calls and subsequent DOM manipulations on the client


### Streaming of Data

* the application just send the rendered html template

* the data is streamed to the client at the time it is available



# Resources


## Frameworks

* Those could be inspiration for client-server communication

> https://github.com/bigpipe/bigpipe

> http://oboejs.com/


## Libs

* https://www.npmjs.org/package/koa-jsonp

* https://github.com/Raynos/http-framework



## Swagger Standard (Now Open API)

* https://openapis.org/

## Dictionary

* We have Specification / Endpoints / Parameters / Definitions

**Specification** 

Swagger is specification how to describe APIs so the consumer would be able to use them

It allows you to document your API so consumers understand the endpoints, parameters, and responses.

Swagger documents are validated with JSON schema https://github.com/OAI/OpenAPI-Specification/blob/master/schemas/v2.0/schema.json that can be consumed with the following npm module https://www.npmjs.com/package/swagger-schema-official

**Definitions**

Definitions allow you to define the format and types of data sent and received by your API.

Basically these are yours domain models!

**Endpoints**

Callable URLs that are basically operations - we can use them to send or get data from. This is the communication interface.

**Parameters**

The things we should pass to invoke operation or receive as a result of particular operation


## The goal of Swagger™

To define a standard, language-agnostic interface to REST APIs which allows both humans and computers

To discover and understand the capabilities of the service without access to source code, documentation, or through network traffic inspection

When properly defined via Swagger, a consumer can understand and interact with the remote service with a minimal amount of implementation logic.

Similar to what interfaces have done for lower-level programming, Swager removes the guesswork in calling the service.


## Resources

### Consume in JS 

Alternatives may be ?

1) This modules gives us the possibility to take JavaScript object based on swagger enabled API - https://github.com/swagger-api/swagger-js

2) What is the difference with this one -> https://github.com/BigstickCarpet/swagger-parser

3) https://github.com/apigee-127/swagger-tools and https://github.com/apigee-127/swagger-tools/blob/master/docs/API.md

* Schema validators 

https://github.com/zaggino/z-schema

* Swagger ref parser 

https://www.npmjs.com/package/json-schema-ref-parser



### Other

* editor.swagger.io

> online editor for swagger documents with live preview


* Further explanations of why we would need standartiosation in APIs area

> http://strongloop.com/strongblog/api-conventions-standards-apps-world-2014/


* Swagger Node.js implementation

> https://github.com/silas/swagger-framework


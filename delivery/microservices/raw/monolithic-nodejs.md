# Source

> http://www.richardrodger.com/monolithic-nodejs

> http://senecajs.org/


#tl;dr

* Explains why architecting with Node.js is intuitive

* Introduces MicroServices and Programmer Anarchy concepts and their implementation - senecajs

# Summary

* Monolithic systems are bad

* Modular systems are good

* Objects are hell

* Just because patterns work does not mean they are good and we have to use them. 

* Node.js modules are done right

* As an accident of history, JavaScript has no built-in module system (at least, not yet).

> This weakness has turned out to be a hidden strength.

> Not only has it created the opportunity to experiment with different approaches to defining modules, 
> but it also means that all JavaScript module systems must survive within the constraints of the language. 

> Modules end up being local variables that do not pollute the global namespace.
> This means that module A can load version 1 of module C, and module B can load version 2 of module C, and everything still works.

* Modules are better than objects

> Modules also naturally tend to have a much lower public API to code ratio.

> They are far more encapsulated than objects.

> You can’t as a rule misuse them in the same way objects can be misused.

> The only real way to extend modules is to compose them into new modules, and that’s a good thing.

* Node.js patterns are simple

> If you come from a language that supports threads, this seems like a killer blow.

> How can you possibly build real systems? The are two things that you do. 

1) You delegate concurrency to the operating system, using processes instead of threads. 

2) And you avoid CPU intensive tasks in code that needs to respond quickly. Put that work on a queue and handle it asynchronously. 
This turns out to be more than sufficient in practice.


* Node.js does require you to learn some new patterns, but they are few in number

> Callback

> Chaining

> Asynch code

> Streams


* Thinking at the Right Level

> Our programming languages should let us think at the right level, the level of the problems we are trying to solve.

> Most languages fail miserably at this. To use an analogy, we’d like to think in terms of beer, but we end up thinking in terms of the grains that were used to brew the beer.

> Our abstractions are at too low a level, or end up being inappropriate.

> Our languages do not enable us to easily compose their low level elements into things at the right level.

> The complexity in doing so trips us up, and we end up with broken, leaky abstractions.

**To build large-scale systems you need to represent this action-oriented way of looking at the world. This is why design patterns fail. They are all about static representations of perfect ontologies. The world does not work like that. Our brains do not work like that.**

* Micro-Services

> The micro-services approach is a radically different way of building systems.

> The services each perform a very limited task.

> This has the nice effect that they are easy to verify.

> You can eye-ball them. Testing is much less important.

1) easy to rewrite

2) easy to scale

3) easy to communicate

* Micro services must be composed with pattern matching.

> There is a framework about it - http://senecajs.org/






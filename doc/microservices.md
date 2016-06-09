Back to [TOC](../Readme.md)

![Nodezoo][Logo]

# Microservices

Microservices are a software component model that works. They are a way of making big software systems out of little pieces. Little pieces of software are easy to understand, easy to
reason about, and easy to inspect for correctness.

Large scale software systems are best built using a component architecture that makes composition both possible and easy. The term microservice captures two important
aspects of this idea. The prefix indicates that the components are small, avoiding micro accumulation of technical debt. In any substantial system there will be many small
components, rather than fewer large ones. The root indicates that the components service should not be constrained by the limitations of a single process or machine, and should be
free to form a large network. Components, that is, microservices, are able to communicate with each other freely. As practical matter, communication via messages,
rather than shared state, is essential to scaling the network.

That said, the heart of the microservice idea is bigger than these two facets. It is the more general idea that composable components are the units of software construction,
and that composition works well only when the means of communication between components is sufficiently uniform to make composition practical. It is not the choice of
the mechanism of communication that matters. What matters is the simplicity of the mechanism.

The core axioms of the microservice architecture are:

  * no components are privileged (privilege);
  * all components communicate in the same simple way (uniform communication);
  * components can be composed from other components (composition).

From these axioms fall out the more concrete features of the microservice architecture. Microservices in practice are small, because the smaller you are, the easier
you are to compose. And if you’re small, it matters a great deal less what your implementation language is. In fact, you may be completely disposable, as rewriting your functionality is not that much work.

Microservices communicate over the network using messages. In this way they share a surface feature with service-oriented architectures.
Is it immaterial to the microservice architecture what data format the messages use, or the protocols by which they are transported. 
Microservices are entirely defined by the messages they accept, and the messages they emit. From the perspective of an individual microservice instance, and from the perspective of the developer writing that
microservice, there are only messages arriving, and messages to send. In deployment, that microservice instance may be participating in a request/response configuration, or a
publish/subscribe configuration, or any number of variants. The way in which messages are distributed is not a defining characteristic of the microservice architecture. All distribution strategies are welcome without prejudice .

The above description is from [The Tao of Microservices](https://www.manning.com/books/the-tao-of-microservices)


# Resources

 * [The Tao of Microservices](https://www.manning.com/books/the-tao-of-microservices)
 * [Solving service discovery](https://www.youtube.com/watch?v=67POODXANi8)
 * [Node.js microservices without a registry](https://www.youtube.com/watch?v=9VC6YeQeZVk)
 * [Measuring Microservices](https://www.youtube.com/watch?v=iEB0BlenAEo)
 * [Richard Rodger talking at first ever microservices Dublin meetup](https://www.youtube.com/watch?v=eTpLNhQJyyc)

[Logo]: https://raw.githubusercontent.com/nodezoo/nodezoo-org/master/assets/logo-nodezoo.png

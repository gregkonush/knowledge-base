
- During build time Quarkus removes classes that won't be need at a runtime.

- Quarkus tries to avoid reflection to reduce startup time.

- Native executables have first-class support. Quarkus uses agressive dead-code elimination techniques to only embed the part of the JVM and classes that
  are absolutely required by an application.

## Reactive architechture

[Reactive Manifesto](https://www.reactivemanifesto.org/)

Reactive Systems as distributed systems having four characteristics:

- Responsive - they must respond in a timely fashion
- Elastic - they adapt themselves to the fluctiating load
- Resilient - they handle failures gracefully
- Asynchronous message passing - the component of a reactive system interact using messages

### How does Quarkus enables Reactive

Under the hood, Quarkus has a reactive design. It is using Eclipse Vert.x and Netty, handles the non-blocking I/O interactions.

### There are two ways how to write reactive code in Quarkus

- Reactive Programming with [Mutiny](https://smallrye.io/smallrye-mutiny)

  - An intuitive, event-driven reactive programming library.

- Coroutines with Kotlin

  - Co-routines are a way to write asynchronous code sequentially.

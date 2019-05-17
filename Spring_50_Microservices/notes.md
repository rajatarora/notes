# Chapter 1

## 1. Why are microservices a thing?

### a. The business said so.

    - Modern businesses are agile.
    - They can no longer afford to build software that takes years to release.
    - They want to quickly add incremental features to their applications and do it in a non-risky, non-expensive way.
    - They even want to change their implementation quickly if they don't perform as expected.

### b. The technology said so.

    - Development paradigms are changing.
    - It is a lot easier to build microservices than a decade ago.
    - Frontend frameworks like React can take care of adaptive designs.
    - Schemaless databases like Mongo can take care of adaptive data storage.
    - Docker and Kubernetes can take care of adaptive deployments.
    - Microservices don't mind polyglot applications.

## 2. Hexagonal Architecture

    The Hexagonal Architectural Pattern dictates that any business logic should be encapsulated from the rest of the world. It should not concern itself with how data is being ingested, transferred, stored, or egressed. Ports and adapters at the edge of the business functions convert the myriad inputs into a common format understood by the core logic.

    This leads to a decoupling of data ingress mechanism and data processing mechanism, and each can be changed / replaced without the other knowing about it.

## 3. Microservice definition

    There is no standard definition for microservices. According to Martin Fowler however:

    > It is an approach to developing a single application as a suite of small services, each running in its own process and communicating with lightweight mechanisms (HTTP, protobuf, etc.)

    Microservices are also supposed to be independently deployable via an automated process. They can each be written in a different language too, all the while supporting different functionalities of a single application. They are autonomous, self-contained, and loosely coupled.

## 4. 3-tier vs Microservices

    
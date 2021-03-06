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

A traditional 3-tier architecture consists of a Presentation layer (which consists of UI and display-related logic), a Business layer (which consists of all application logic), and a Database layer (which contains all the data). If a particular application consists of say two modules, the Presentation layer and the Business layer both contain two submodules each, and the database is shared by both modules.

If there is a change in the Business layer of module-2, the entire layer has to be redeployed. Similarly, if some maintenance activity is to be performed to a part of database used by module-1, the entire database has to be take offline and the activity performed.

Microservices, on the other hand, encapsulate the entire application into a separate application. Each service has its own presentation layer, business layer, and even database.
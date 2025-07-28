# 🏛️ Software Architecture Overview

A curated summary of the most used software architectures in modern backend and enterprise systems. This guide is intended to help engineers, architects, and hiring managers understand how I think, build, and scale software systems.

---

## 🧱 Contents

- [Layered Architecture (N-tier)](#layered-architecture-n-tier)
- [Microservices Architecture](#microservices-architecture)
- [Event-Driven Architecture](#event-driven-architecture)
- [CQRS and Event Sourcing](#cqrs-and-event-sourcing)
- [Hexagonal Architecture (Ports & Adapters)](/examples/hexagonal.md)
- [Domain-Driven Design (DDD)](#domain-driven-design)
- [Bonus: Clean Architecture](#clean-architecture)

---

## 📚 Layered Architecture (N-tier)

The traditional model with clear separation between presentation, business logic, and data access layers.

✅ Easy to implement  
⚠️ Tight coupling and hard to scale for large systems

---

## 🧩 Microservices Architecture

Each service is independently deployable, responsible for a single business capability.

✅ Scalable, fault-isolated, deployable  
⚠️ Operational complexity, distributed tracing

![Microservices Diagram](./diagrams/microservices.png)

---

## 📬 Event-Driven Architecture

Systems communicate asynchronously using events and message brokers (e.g., RabbitMQ, Kafka, AWS SQS).

✅ Loose coupling, real-time capabilities  
⚠️ Harder to debug, requires eventual consistency

---

## ⚔️ CQRS & Event Sourcing

CQRS separates read and write models; Event Sourcing stores events instead of the current state.

✅ Great for audit trails, performance  
⚠️ Steeper learning curve, eventual consistency

---

## 🛠 Hexagonal Architecture (Ports & Adapters)

Also known as Clean Architecture. Core business logic is isolated from infrastructure and UI.

✅ Highly testable, independent of frameworks  
⚠️ May feel over-engineered for simple projects

---

## 🧠 Domain-Driven Design (DDD)

Focuses on modeling complex domains using rich domain models and bounded contexts.

✅ Aligns software design with business needs  
⚠️ Requires close collaboration with domain experts

---

## 🧼 Bonus: Clean Architecture

A way of structuring systems so that business logic doesn't depend on frameworks, databases, or UI.

---

## 🔗 References & Tools

- [Microsoft Architecture Center](https://learn.microsoft.com/en-us/azure/architecture/)
- [DDD Patterns](https://dddcommunity.org/)
- [Microservices.io](https://microservices.io/)

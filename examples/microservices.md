# 📦 Microservices Architecture

Microservices is an architectural style that structures an application as a collection of loosely coupled, independently deployable services.

## ✅ Key Characteristics

- Each service has its own database and bounded context
- Services communicate via HTTP/REST, gRPC, or messaging queues (RabbitMQ, Kafka)
- Independently deployable and scalable
- Enables small, focused teams per service

## 🧰 Typical Tech Stack

- .NET Core + WebAPI
- Docker + Kubernetes
- RabbitMQ / AWS SQS / Apache Kafka
- Redis for caching
- MongoDB / PostgreSQL / DynamoDB (per service DB)

## 💡 Example Use Case

A banking system with independent services:

- `AccountsService`: Manages customer accounts
- `PaymentsService`: Processes incoming/outgoing payments
- `CreditAnalysisService`: Handles credit scoring and rules
- `NotificationService`: Sends emails/SMS

Each service has its own CI/CD pipeline, database, and can scale independently.

## 🔗 Pros & Cons

**Pros:**
- Scalability
- Technology diversity
- Fault isolation

**Cons:**
- Increased complexity
- Requires DevOps maturity
- Distributed tracing/debugging

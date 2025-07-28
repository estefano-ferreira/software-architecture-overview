# ⚔️ CQRS & Event Sourcing

CQRS (Command Query Responsibility Segregation) and Event Sourcing are patterns for managing complex business logic and state changes in modern systems.

## ✍️ CQRS Overview

CQRS separates the read and write responsibilities:

- **Commands** change the state of the system
- **Queries** return data without modifying it
- Improves scalability and allows independent optimization

## 📜 Event Sourcing Overview

Instead of storing only the current state, every change (event) is recorded:

- State is rebuilt by replaying events
- Useful for audits, traceability, and debugging

## 🧰 Typical Stack (C# / .NET)

- MediatR for command and query handling
- EventStoreDB or custom event table in SQL/PostgreSQL
- Projectors to build denormalized read models
- Kafka/RabbitMQ for publishing events

## 💡 Example Use Case

A Loan Application system might use:

1. `ApplyForLoanCommand`
2. Results in `LoanAppliedEvent`
3. Event is stored and triggers other actions (email, approval workflow)
4. Read model is updated for reporting UI

## ✅ Benefits

- Clear separation of concerns
- Event replay and auditing
- Supports distributed, scalable systems

## ⚠️ Considerations

- More moving parts (event store, projectors, consistency)
- Requires well-defined domain events

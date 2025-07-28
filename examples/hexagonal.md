# 🛠 Hexagonal Architecture (Ports & Adapters)

Hexagonal Architecture isolates core business logic from infrastructure, allowing flexibility and high testability.

## 🧩 Core Concepts

- **Core (Domain + Application)**: contains business rules and use cases
- **Ports**: interfaces that define how the outside world interacts with the core
- **Adapters**: implementations of those interfaces (e.g., database, HTTP clients)

## 🧰 Typical Structure in .NET


# 🛠 Hexagonal Architecture (Ports & Adapters)

Hexagonal Architecture isolates core business logic from infrastructure, allowing flexibility and high testability.

     /src
     ├── Application
     │   ├── Interfaces # Input/output ports
     │   └── UseCases # Business logic
     ├── Domain
     │   ├── Entities
     │   ├── ValueObjects
     │   └── DomainEvents
     ├── Infrastructure
     │   ├── Repositories # EF Core / MongoDB
     │   ├── Email # SMTP implementations
     │   └── APIClients # External service integrations
     └── WebAPI
         ├── Controllers
         └── Program.cs



## 🧠  Layers and Responsibilities

🔷 **Application**  
     - Contains the application use cases (e.g., CreateLoan, RegisterCustomer).  
     - Defines interfaces (ports) that will be implemented externally.  
     - Does not depend on infrastructure or frameworks.

🧩 **Domain**  
     - The heart of the business logic, completely pure.  
     - Defines entities, value objects, and domain events.  
     - Can be tested in isolation.

⚙️ **Infrastructure**  
     - Implements the Application interfaces (adapters).  
     - Integrates with external technologies: databases, services, messaging, etc.  
     - Examples: CustomerRepository with EF Core, EmailSender with SMTP.

🌐 **WebAPI**  
     - Layer responsible for exposing the application via HTTP.  
     - Contains controllers and the Program.cs file.  
     - Receives requests, invokes use cases, and returns responses.
     
## 🔗 References & Tools
- [Common web application architectures](https://learn.microsoft.com/en-us/dotnet/architecture/modern-web-apps-azure/common-web-application-architectures#domain-driven-design-ddd)

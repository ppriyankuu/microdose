## Decomposition
Decomposition refers to breaking down a monolithic application into smaller, independent, and loosely coupled services. Each service should focus on a single responsibility and be capable to scaling independently. Proper decomposition is crucial for maintaining a clean architecture, ensuring modularity, and enabling efficient development and deployment.

Different Scenarios and bases for decomposition:
1. **Domain-Driven Design (DDD)**: Focus on aligning software design with business domains. It emphasizes understanding the business context and modeling software around core business concepts.
    How to Decompose:
    - Identify key business domains and subdomains.
    - Create bounded contexts within these domains, where each bounded context represents a cohesive set of functionality.

    e.g., consider an e-commerce platform. The primary domains could be:
    - Customer Management: Handles user accounts, profiles, and authentication.
    - Product Management: Manages products, categories, and inventory.
    - Order Processing: Manages order creation, status updates, and fulfillment.
    - Payment Processing: Handles transactions and billing.

    Using DDD:
    - ensures alignment with business processes.
    - promotes clear boundaries and responsibilities.
    - facilitates collaboration between developers and domain experts.
2. **Function Decomposition**: Involves breaking down an application into smaller components based on the functions they perform.
    How to Decompose:
    - Identify major functional areas.
    - Split these areas into smaller, more focused services.

    e.g., for a social media platform, the main functional areas could be:
    - User profile management: Handles user data, settings, and preferences.
    - Post management: Manages posts, comments, like, and shares.
    - Notification system: Sends notifications for new messages, friend requests, etc.
    - Analytics: Provides insights into user behavior and engagement.

    Using functional decomposition:
    - simplifies understanding of the application.
    - makes it easier to scale individual functions independently.
    - allows for specialised expertise in each area.

#### Other Decompositional Techniques
Microservices offer flexibility due to their granular nature, but other decomposition methods also try to deliver similar benefits.
**Shared Libraries**
Shared libraries allow code reuse across teams and services, enabling better organisation. However, they have limitations: loss of technology heterogeneity, restricted independent scaling, the need to reploy entire processes for changes, and fewer opportunites to build reliency. Shared libraries are good for common, non-domain-specific code but can introduce unwanted coupling if used for service communication.

**Modules**
Same languages offer modular decomposition beyond basic libraries. OSGI (in Java) tried to provide module lifecycle management, but due to lack of native support, it often adds complexity. Erlang, however, bakes modularity into the runtime, supporting smooth upgrades and mulitple module versions. Despite these capabilities, modules still suffer the same issues as shared libraries; technology restrictions, scaling challenges, and hidden coupling risks. In practice, even well-structured modules within monoliths tend to become tightly coupled over time. Process boundaries in microservices help enforce better separation, which alone rarely achieve.

**No Silver Bullet**
Microservices are not a free solution; they bring the complexity of distributed systems. to succeed, organisations must improve deployment, testing, monitoring, and system resilience. Adopting microservices also demands understanding challenges like distributed transactions and the CAP theorem. Whether microservices fit a system depends heavily on the the specific context.
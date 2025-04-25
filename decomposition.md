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
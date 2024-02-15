# BudgetBuddy
Creating a full Splitwise project with end-to-end code in Java, along with detailed explanations, would be quite extensive for a single response. However, I can provide you with a high-level overview of the project structure, technologies, and architecture you might consider, and guide you through the main components and functionalities. Let's break it down:

### Technologies Used:
1. **Backend Development:**
   - Language: Java
   - Framework: Spring Boot (for RESTful API development, dependency injection, and MVC)
   - Database: PostgreSQL or MySQL (for storing user data, expenses, groups, etc.)
   - ORM Framework: Hibernate (for database interaction and mapping Java objects to database entities)
   - Security: Spring Security (for user authentication and authorization)
   - Messaging: RabbitMQ or Kafka (for asynchronous processing and notifications)
   - Testing: JUnit and Mockito (for unit and integration testing)

2. **Frontend Development:**
   - HTML, CSS, JavaScript
   - Framework: React.js or Angular (for building interactive UI components)
   - State Management: Redux or Context API (for managing application state)

### Project Structure:
1. **Backend:**
   - **Controllers:** Handle incoming HTTP requests, call services, and return responses.
   - **Services:** Implement business logic, interact with repositories, and perform CRUD operations.
   - **Repositories:** Communicate with the database, execute queries, and manage database entities.
   - **Models:** Define data structures and entities used within the application.
   - **Security Config:** Configure authentication and authorization rules.
   - **Configuration:** Application configuration settings, database connection, etc.
   - **Messaging:** Configuration for message brokers and listeners for asynchronous processing.
   - **Tests:** Unit tests for services, controllers, and repositories.

2. **Frontend:**
   - **Components:** Reusable UI components like forms, buttons, headers, etc.
   - **Pages:** Different pages of the application like login, dashboard, group management, expense tracking, etc.
   - **Services:** Functions to make HTTP requests to backend APIs and handle responses.
   - **Redux (or Context) State:** State management logic and actions for managing user data, groups, expenses, etc.
   - **Styles:** CSS files for styling the components.
   - **Tests:** Unit tests for components and services.

### Architecture:
1. **Backend Architecture:**
   - **Layered Architecture:** Separation of concerns with layers like Controller, Service, Repository.
   - **RESTful API:** Expose endpoints for frontend interaction following REST principles.
   - **Microservices (Optional):** If scalability and modularity are required, split functionalities into separate microservices.

2. **Frontend Architecture:**
   - **Component-Based:** Break UI into reusable components with well-defined responsibilities.
   - **State Management:** Centralized state management for better organization and scalability.
   - **Responsive Design:** Ensure the UI is responsive and accessible across different devices and screen sizes.

### Detailed Explanation:
1. **User Management:**
   - Allow users to register, log in, log out, and update their profiles.
   - Implement authentication using JWT tokens or session-based authentication.
   - Secure endpoints with authentication and authorization checks.

2. **Group Management:**
   - Users can create new groups, add members, remove members, and configure group settings.
   - Groups can have multiple members, and each member can contribute to expenses within the group.

3. **Expense Tracking:**
   - Users can add expenses, specify the payer, participants, amount, description, and category.
   - Expenses can be equally split, custom split, or split by percentage among participants.

4. **Debt Calculation:**
   - Compute and maintain debt balances between users within each group.
   - Update debt balances when new expenses are added or settled.

5. **Notifications:**
   - Send real-time notifications to users for expense updates, reminders, and group activities.
   - Use messaging queues for asynchronous processing and scalability.

6. **Payment Integration:**
   - Integrate with third-party payment gateways like PayPal or Stripe for settling debts.
   - Allow users to initiate transactions securely within the application.

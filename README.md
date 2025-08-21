# CS 230 Software Design Portfolio

## Project: Draw It or Lose It - Web-Based Game Platform

### Client Summary
The Gaming Room is a mobile game developer that currently has their game "Draw It or Lose It" available only on Android. They wanted us to design a web-based version that could run in any browser while maintaining the same gameplay experience. The software needed to support multiple teams per game, multiple players per team, ensure unique naming for all entities, and be scalable for future growth. The main requirement was creating a singleton GameService that manages all game instances and ensures data integrity across the platform.

### Documentation Strengths
What I did particularly well was creating a comprehensive evaluation of different operating platforms and their suitability for both server and client-side deployment. I thoroughly analyzed Linux, Windows, Mac, and mobile platforms, considering factors like cost, performance, and development tools. I also excelled at designing the domain model with clear UML diagrams that showed the inheritance hierarchy and relationships between Game, Team, and Player entities. The use of design patterns like Singleton and Iterator was clearly documented with explanations of why each pattern solved specific client requirements.

### Design Document Benefits
Working through the design document helped during development by providing a clear roadmap of the system architecture before writing any code. Having the UML diagram meant I understood exactly how Game, Team, and Player classes should interact and inherit from the Entity base class. The document's requirement section forced me to think through edge cases early, like ensuring unique names and IDs, which prevented major refactoring later. The platform evaluation section helped me make informed decisions about development tools and deployment strategies rather than discovering limitations during implementation.

### Areas for Improvement
If I could revise one part, I would expand the System Architecture View section with a more detailed diagram showing the client-server communication flow, API endpoints, and data flow between components. Currently, it mentions that "we do not need a full architecture diagram," but having one would better communicate the technical implementation to developers. I would add sequence diagrams showing how a typical game session works from player login through gameplay to score recording. This would make it easier for new developers to understand the system without diving into code.

### User Needs Implementation
I interpreted user needs by translating business requirements into technical specifications - for example, the need for "no duplicate names" became a validation loop in the GameService that checks existing entities before creation. Understanding that players might disconnect and reconnect led to designing a stateless server architecture that maintains game state centrally rather than in user sessions. This was crucial because users expect seamless gameplay experiences without losing progress, and considering their needs upfront prevented frustrating user experiences. I made sure the design supported both current needs (web-based play) and future scalability (cloud deployment, mobile apps).

### Software Design Approach
My approach to designing software involved starting with understanding the problem domain through requirements gathering, then creating visual models (UML diagrams) to represent the system structure. I used object-oriented principles like inheritance, encapsulation, and abstraction to create reusable, maintainable code. I applied proven design patterns (Singleton, Iterator) to solve specific architectural challenges. In the future, I would use domain-driven design to better model complex business logic, implement test-driven development to ensure requirements are met, and create more detailed API specifications using tools like OpenAPI/Swagger. I would also incorporate more security considerations earlier in the design phase rather than treating it as a separate concern, and use microservices architecture for better scalability from the start.

## Technologies Recommended
- **Server Platform:** Ubuntu Server 22.04 LTS on cloud providers (AWS/Azure/GCP)
- **Architecture:** Monolithic initially, with path to microservices
- **Database:** PostgreSQL with Redis caching
- **Security:** TLS 1.3, JWT authentication, bcrypt password hashing
- **Deployment:** Docker containers with Kubernetes orchestration

## Repository Contents
- `CS 230 Project Software Design Template.docx` - Complete software design document
- `README.md` - This reflection document

## Author
Sarvarbek Fazliddinov  
CS 230 - Operating Platforms  
Date: [Current Date]

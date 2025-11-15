Team Roles

1. Project Manager

Responsible for overseeing the entire project. Ensures tasks are completed on time, coordinates communication between team members, manages timelines, and removes roadblocks to keep the team aligned.

2. Backend Developer

Designs, builds, and maintains the server-side logic of the application. Responsible for creating APIs, integrating databases, handling authentication, and ensuring the system is secure, scalable, and performant.

3. Frontend Developer

Implements the user interface and user experience of the application. Works with frameworks like React, Vue, or Angular to develop responsive, accessible, and interactive features that connect to backend APIs.

4. Database Administrator (DBA)

Manages the project’s database systems. Responsible for database design, optimization, security, backups, and ensuring efficient data storage and retrieval.

5. DevOps Engineer

Responsible for automation, deployment pipelines, CI/CD, server configuration, and monitoring. Ensures the application runs reliably across different environments (development, staging, production).

6. Quality Assurance (QA) Engineer

Tests the application to ensure quality and stability. Responsible for identifying bugs, writing test cases, performing manual and automated tests, and ensuring all features meet requirements before release.

7. UI/UX Designer

Designs the overall look, feel, and flow of the application. Responsible for creating wireframes, mockups, user journeys, and ensuring the product is user-friendly and visually appealing.

8. Business Analyst

Gathers and analyzes the project requirements. Ensures the development team clearly understands user needs and that the final product aligns with business goals.

9. Security Specialist

Ensures the application is safe from vulnerabilities. Responsible for reviewing code for security flaws, implementing best security practices, and monitoring for threats.

Technology Stack

1. Django

A high-level Python web framework used to build robust backend systems.
Purpose: Provides the server-side logic, RESTful API endpoints, authentication, and core business functionalities.

2. Django REST Framework (DRF)

A powerful toolkit built on Django for creating Web APIs.
Purpose: Simplifies API development, serialization, authentication, and permissions.

3. GraphQL

A query language for APIs that allows clients to request exactly the data they need.
Purpose: Enables efficient data fetching and reduces the number of requests between client and server.

4. PostgreSQL

A reliable and scalable relational database system.
Purpose: Stores and manages structured project data with strong support for complex queries and relationships.

5. Redis

An in-memory data structure store used as a cache and message broker.
Purpose: Speeds up application performance by caching frequently accessed data and supporting background task queues.

6. Docker

A containerization platform for packaging and running applications consistently across different environments.
Purpose: Ensures the backend, database, and other services run in isolated containers for easier deployment and development.

7. Nginx

A high-performance web server and reverse proxy.
Purpose: Handles incoming client requests, serves static files, and forwards API requests to the backend application.

8. Git & GitHub

Version control and cloud repository hosting platform.
Purpose: Tracks code changes, supports collaboration, and stores the project codebase.

Database Design

1. Users

Represents individuals who use the platform as guests or property owners.
Key Fields:

id – unique identifier

name – full name of the user

email – unique email address for login

role – defines whether the user is a guest or property owner

created_at – date the account was created

2. Properties

Represents the accommodation listings created by property owners.
Key Fields:

id – unique identifier

owner_id – references the user who owns the property

title – property name/title

location – property address or city

price_per_night – cost of booking per night

3. Bookings

Represents reservations made by users for specific properties.
Key Fields:

id – unique identifier

property_id – property being booked

user_id – user who made the booking

start_date – check-in date

end_date – check-out date

4. Payments

Tracks payment information related to bookings.
Key Fields:

id – unique identifier

booking_id – booking associated with the payment

amount – total amount paid

payment_method – e.g., credit card, PayPal, etc.

status – e.g., pending, completed

5. Reviews

Represents user feedback for properties.
Key Fields:

id – unique identifier

property_id – property being reviewed

user_id – user leaving the review

rating – numeric rating (e.g., 1–5)

comment – written review

Entity Relationships

A User can own multiple Properties, but each Property belongs to one User (1-to-many).

A User can make many Bookings, but a Booking belongs to one User (1-to-many).

A Property can have multiple Bookings, but each Booking is linked to one Property (1-to-many).

A Booking has one Payment, and a Payment is tied to one Booking (1-to-1).

A Property can have many Reviews, but each Review is posted by one User (many-to-1).

A User can write many Reviews, but each Review belongs to one Property (1-to-many).

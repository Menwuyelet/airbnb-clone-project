# Airbnb Clone Project

- This project is a simplified clone of the backend of Airbnb platform that provides core functionalities for managing user interactions, property listings, bookings, and payments processing. The technologies such as Django, Django RESTframework, PostgreSQL, GraphQL, Redis, Docker, Celery, and CI/CD Pipelines are used to implement its functionalities and achieve its goals.

## Team Roles

- In order to achieve the project goals there should be a role distribution in the team. Below are the key roles for the backend of Airbnb Clone Project and their responsibilities:

1. Backend Developer: Is the team member that is responsible for implementing API endpoints, database schemas, and business logic of the project.
2. Database Administrator: Is the team member that is responsible for designing the database of the system, indexing, and database optimizing to increase performance of the system.
3. DevOps Engineer: Is the team member that handles deployment, monitoring the system after deployment, and scaling of the backend services as the data and business grows.
4. QA Engineer: Is the team member that is responsible for ensuring the backend functionalities are thoroughly tested and meet quality standards.

-- I didn't include team roles such as UI/UX designer, Project owner and Business analyst as these roles are more of a fullstack team roles and out of our projects scope.

## Technology Stack

- To achieve the project goals different technologies are used for different purpose.

1. Django - It is a high-level Python web framework used for building fullstack web apps (specially backends).
2. Django RESTframework - It is a toolkit built on top of Django used for building the RESTful backend of the project (the API).
3. PostgreSQL - It is a relational database management system used to store data in secure database and relational modeling of entities in the project.
4. GraphQL - It is a query language for APIs and a runtime for executing those queries. it allows flexible and efficient querying of data providing performance increase in the project.
5. Celery - It is a tool used to handle background jobs by running tasks asynchronously. it is used in the project to process payments, sending notifications and sending emails for booking confirmation and other purposes without interrupting the performance of the main django app.
6. Redis - It is in-memory key-value data store. in the project it is used for caching, session management and as message broker from django to Celery.
7. Docker - It is a containerization platform that is used to package applications and their dependencies in to a unit called container. in the project it is used to containerize the project and all its dependencies for isolation and consistency.
8. CI/CD Pipelines - are automated pipelines for testing and deploying code changes. it is used in the project to automate tests for ensuring bug free code and to automate deployment after updating the code base for fast and easy updating.


## Database Design

- The key entities in this project with their attributes are:
1. Users with attributes such as: user_id, user_name, first_name, last_name, contact, is_host
2. Property with fields: property_id, host, location, price, description
3. Booking wit fields: booking_id, guest, property, start_date, end_date, status
4. Payment with fields: payment_id, booking, amount, payment_date, status
5. Review with fields: review_id, author, property, rating, description, created_at

- These entities has a relation ship one wit other such as:
* a user can host multiple Properties, can make many Bookings, can author multiple Reviews.
* each Property belongs only to one Host, can have many Bookings and can have many Reviews.
* each Booking belongs to one property and one gust
* each review is written by one User for one Property.
* each Payment is for one Booking and one Booking can have multiple Payments.

##  Feature Breakdown

- The project offers features such as managing user interactions, property listings, bookings, and payments processing. each feature contributes to the project in its own way that is:
1. Managing User Interactions: This feature handles user registration, authentication, and profile management, enabling secure access and personalized experiences. making the project secure and efficient.
2. Property Listings: Property owners can create, update, and manage listings by adding descriptions, prices, and availability. This allows users to browse properties easily filtering based on preferences,  available, prices and make informed decisions.
3. Bookings: This feature allows users to book properties for specific dates, handling availability checks and conflict prevention. It plays a central role in the main goal of the project connecting property owners with potential renters in a smooth and organized way.
4. Payments Processing: Secure payment integration ensures that users can pay for bookings directly through the platform. It automates transaction handling, supports multiple payment methods, and ensures both users and hosts receive the desired service with ease.


## API Security

- To insure the project is secure, several security measures are implemented such as:
1. Authentication: It is a method used to ensure that only legitimate users can access the system. to achieve this token-based authentication is used. it is important to protect personal data form unauthorized use and enabling for authorization the other security measure used in the project to insure the security of the system.
2. Authorization: It is a method used to control what authenticated users are allowed to do in the system. it is crucial because it ensures that users can only see their own bookings, profiles and edit only their profiles. for property users it only allows the owner of that specific property is allowed to offer the property to users and manage it.
3. Rate Limiting - Rate limiting is used to control network traffic in order to avoid system overload. it restricts the number of requests a user can make to the system within a certain time frame. it contributes to the project security by preventing brute-force login attacks and denial-of-service attacks.
4. Input Validation & Sanitization: It is the process of checking and cleaning of input data from users to prevent malicious data from entering the system. it contributes to the systems security measure by preventing attacks such as SQL injections and cross site scripting(XSS).
5. Secure Payment Processing: It is a multi stage approach to ensure the confidentiality, integrity and authenticity of financial transactions through encryption, authentication and fraud detection. it contributes to the systems security by providing a secure way to perform one of the core feature of the system which is payment processing.

- The security of the system is very important because the system handles very sensitive data such as financial information of the users, property details and different personal details. by implementing the security measures mentioned above will make the system trust worthy and safe.

## CI/CD Pipeline

- CI/CD (Continuous Integration and Continuous Deployment) pipelines:  are a series of steps that automate the process of testing code changes before integrating them to the code base permanently ensuring that the code changes will work with the existing code base and deploying code changes to automatically update the application based on the code changes.
- CI/CD pipelines are important to the project as they allow us to develop and deploy easily and rapidly by insuring code integration and correctness via automated tests and deploying code changes easily by automated deployment.
- There are several tools that are used to implement CI/CD pipelines such as: 
1. GitHub Actions: Is a CI/CD platform that allows to automate project build, test and deployment directly form the GitHub repository.
2. Docker: It is a platform that uses containerization technology to build, test, and deploy applications.
3. Azure DevOps: Is a platform that provides tools for version control, project management and CI/CD implementations.
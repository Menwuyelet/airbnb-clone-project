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

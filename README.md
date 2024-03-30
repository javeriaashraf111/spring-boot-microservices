# Spring Boot Microservices - Online Shop Application
In this project, we have the following services: 
1. Product Service: Create and View products, acts as a product catalog.
2. Order Service: Through this, we can order products.
3. Inventory Service: Through this, we can check if a product is in stock or not.
4. Notification Service: Through this, we can send Notifications after an order is placed.

# High-Level Design

![High Level Design](https://github.com/javeriaashraf111/spring-boot-microservices/assets/49598949/ea06bc12-2a23-4759-a55e-683a36add68f)

# Logical Architecture of Services

![Logical Architecture Of Services](https://github.com/javeriaashraf111/spring-boot-microservices/assets/49598949/783980cf-d278-4362-918a-5e376c8de64f)

1. We have a controller service and repository layer for each of the services.
2. In the controller layer we are receiving the HTTP request from the clients and from there the business logic is executed on the service layer.
3. We are communicating through a message queue in order service and notification service.
4. We have stored the data in the database so for that we are also going to maintain a repository layer that mainly talks to the database, we have a Postgres and MongoDB database, both of which will follow the same pattern.
5. We have a repository that talks to the database this is how almost all the services are being structured.

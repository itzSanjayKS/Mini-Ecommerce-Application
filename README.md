# Mini-Ecommerce-Application

a full-stack e-commerce solution enabling seamless product browsing, cart operations, and secure payment processing. 
•	Developed a dynamic frontend using React and Tailwind CSS, delivering responsive UI with features like product search, dynamic cart updates, and user login.
•	Architected a robust backend with Java Spring Boot, implementing REST APIs for product listings, user profiles, and order management, integrated with MySQL using Spring Data JPA. 
•	Secured the application with Spring Security and JWT for role-based authentication and authorization.

Technologies: React, JavaScript, Tailwind CSS, Java, Spring Boot, Spring Security, MySQL, AWS, and JWT.

This project has:
three independent microservices:
a.	User Management Microservice: handles user-related operations
b.	Product Management Microservice: manages product catalogues and inventory
c.	Order Management Microservice: processes and manages orders.

Primary Actors:
1)	Admin: responsible for managing the product catalogue and inventory
2)	Customer: browses and purchases products from the catalogue   

Basic Flow:
Product Management:
1.	Admin adds a new product:
•	. Admin submits a new product request with details (name, description, price, quantity)
•	Product service validates the request and creates a new product entity.
•	Product service returns a success response to the admin

2.	Admin updates an existing product:
•	 Admin submits an update product request with updated details (name, description, price, quantity).
•	Product service validates the request and updates the product entity.
•	Product service returns a success response to the admin

3.	Admin deletes a product:
•	Admin submits a delete product request.
•	Product service validates the request and deletes the product entity.
•	Product service returns a success response to the admin

User Management:
1.	User registration: -admin user creation will be done from back end
•	User submits a registration request with details (username, email, password)
•	User service validates the request and creates a new user entity

2.	User profile update:
•	User submits an update profile request with updated details (name, email, address).
•	User service validates the request and updates the user entity.

Order Management:

1.	Customer places an order:
•	Customer submits an order request with product details and quantity
•	Order service validates the request and communicates with the product service to check available quantity.
•	If the requested quantity is available order is created and the quantity for that product will be reduced through Product service.
•	If the requested quantity is not available a message will be sent back to the user saying quantity is not available.
2.	Order cancellation:
•	Customer submits an order cancellation request
•	Order service changes the status of the order to cancelled and updates the product quantity accordingly.
•	Order service will return a success message to the customer.

Role based access management needs to be implemented so that
1)	Only admin user can have access to the Product Management functionality.
2)	Customer can only have access to the orders they have placed.

Scope of the project will be to:
a)	Analyse the requirement.(Status: Implemented & Working)
b)	UI Design.(Status: Implemented & Working)
c)	Database design.(Status: Implemented & Working)
d)	REST endpoint design (i.e designing of REST urls, methods and input data).(Status: Implemented & Working)
e)	Development and Testing. (Status: Completed)
f)	Create a Jenkins pipeline for build test and deployment (Status:On-progress).
g)	Containerize -using docker (Status:On-progress)


To Run Project:
- Run All the microservices, apigateway and eureka server

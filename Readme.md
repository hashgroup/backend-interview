# Backend Developer Interview - Hotel Booking System

You have been assigned the task of building a backend system for a booking engine that will be used by a hotel group.
The system will be built using microservices to ensure scalability and ease of maintenance with a large team.
Your task is to develop three services: Gateway, Identity, and Booking.
Please follow the design system "diagram.png", "Requirements" to implement and submit "Delivery".

### 1. Below are some explains:

##### Gateway Service:
	- Responsible for handling external requests and routing them to the appropriate services.
	- Internal communication with the Identity and Booking services should use GraphQL or gRPC, while public communication can be done via RESTful APIs.

##### Identity Service:
	- Handles user authentication, including login and registration.
	- Generates random JWT (JSON Web Tokens) for user authentication.
	- A User need contains: id, firstname, lastname, created_at

##### Booking Service:
	- Manages hotel bookings, including creating and canceling bookings.
	- A Bookings need contains: id, hotel(id, name), guest(id, lastname, firstname), checkin_time, booking_time, created_at

### 2. Requirements:
	- Develop 3 services for system and public 4 APIs.
		1. register
		2. login
		3. create-booking (must security with JWT Token)
		4. delete-booking (must security with JWT Token)
	- The system should have three isolated source code folders: gateway, identity, and booking. (Can structure like "structure.png")
	- The Identity and Booking services should have separate databases (connection to your localhost database).
	- Have at least two services should be implemented using Java Spring Boot. The third service can be implemented using any programming language of your choice.
	- Can use any opensoruce library to support your development.
	- Internal communication between the Gateway service, Identity service, and Booking service should use GraphQL or gRPC.
	- Public communication can be use RESTful APIs or GraphQL.

### 3. Delivery:
	- Git Repository links have 3 backend servies: gateway, identity, booking
	- Postman collection export contains: 4 APIs

### 4. Very nice to have:
	- Docker compose setup to easy start all services and database
	- All internal service communication use gRPC
	- 1 services implement with Golang or Python
	- Readme document instructs how to run start your services
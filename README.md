RentVideo: A RESTful API for Video Rental 🎬
Project Overview
RentVideo is a simplified online video rental system developed as a RESTful API service using Spring Boot. The service uses MySQL (or an in-memory H2 database for development) to persist data and implements robust authentication and authorization to control access to its resources.

Key Features
The API provides the following core functionalities:

🔒 Authentication and Authorization
Authentication: The service uses Basic Auth for user authentication.

User Roles: It supports two distinct user roles: CUSTOMER and ADMIN.

Public Endpoints: Accessible by anyone, including unauthenticated users (e.g., user registration).

Private Endpoints: Require a user to be authenticated.

Role-Based Access Control: Private endpoints enforce authorization based on user roles. For instance, only ADMINs can manage video details.

👤 User Management
User Registration: Users can create an account by providing an email address, password, first name, and last name.

Password Security: All passwords are securely hashed using BCrypt before being stored.

Default Role: The user role defaults to CUSTOMER if not specified during registration.

Login: Registered users can log in using their email and password via Basic Auth.

📼 Video Management
The system stores essential video details, including Title, Director, Genre, and an Availability Status.

Public Access: Any user (authenticated or not) can browse the list of available videos.

ADMIN-Only Access: Only users with the ADMIN role are authorized to create, update, or delete videos.

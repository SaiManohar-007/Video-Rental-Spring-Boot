RentVideo: A RESTful API for Video Rental 🎬
<p align="center">
A secure and scalable online video rental system built with Spring Boot.
</p>

✨ Features
This project is a simplified RESTful API for managing a video rental platform, focusing on a robust backend implementation.

🔐 Security & Authentication
Authentication: Utilizes Spring Security with Basic Auth for secure user authentication.

Authorization: Implements role-based access control with two distinct roles: CUSTOMER and ADMIN.

Password Hashing: Passwords are never stored in plain text. They are securely hashed using BCrypt.

👤 User Management
Registration: Public endpoint for new users to sign up with their email and a secure password.

Default Role: New users are automatically assigned the CUSTOMER role.

Access Control: Private endpoints are protected, ensuring only authenticated users can access them.

📼 Video Management
Video Catalog: The API stores and manages video details, including Title, Director, Genre, and Availability Status.

Public Browsing: Anyone can browse the full list of available videos.

ADMIN Privileges: Only ADMIN users have the authority to create, update, and delete videos.

🚀 Endpoints
The API is designed with a clear, RESTful structure.

Endpoint	HTTP Method	Description	Access
/api/register	POST	Registers a new user.	Public
/api/videos	GET	Fetches a list of all videos.	Public
/api/videos	POST	Creates a new video.	ADMIN Only
/api/videos/{id}	PUT	Updates an existing video.	ADMIN Only
/api/videos/{id}	DELETE	Deletes a video.	ADMIN Only

🛠️ Tech Stack
Framework: Spring Boot (3.x)

Security: Spring Security

Database: MySQL (default) or H2 (for development/testing)

ORM: Spring Data JPA

Build Tool: Maven

Utility: Lombok for reducing boilerplate code

📦 How to Run
Clone the repository:

Bash

git clone https://github.com/SaiManohar-007/Video-Rental-Spring-Boot.git
cd Video-Rental-Spring-Boot
Configure the database:

For H2 (in-memory, recommended for local dev): No setup needed. The app will run out-of-the-box.

For MySQL: Update src/main/resources/application.properties with your MySQL credentials.

Run the application:

Bash

./mvnw spring-boot:run
(or use the built-in run feature of your IDE like IntelliJ IDEA)

The API will be available at http://localhost:8080.

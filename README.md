RentVideo: A RESTful Video Rental API <p align="center">
  <strong>A secure and scalable online video rental system built with Spring Boot.</strong>
</p>

<p align="center">
  <a href="https://github.com/SaiManohar-007/Video-Rental-Spring-Boot"><img src="https://img.shields.io/badge/Spring%20Boot-2.7+-6DB33F?logo=spring" alt="Spring Boot"></a>
  <a href="https://github.com/SaiManohar-007/Video-Rental-Spring-Boot"><img src="https://img.shields.io/badge/License-MIT-blue.svg" alt="License"></a>
  <a href="https://github.com/SaiManohar-007/Video-Rental-Spring-Boot/stargazers"><img src="https://img.shields.io/github/stars/SaiManohar-007/Video-Rental-Spring-Boot" alt="Stars"></a>
</p>

 OverviewRentVideo is a RESTful API designed for managing an online video rental platform. It provides a robust backend implementation with a focus on security, scalability, and ease of use. Whether you're browsing the video catalog or managing content as an admin, RentVideo ensures a seamless experience. FeaturesSecurity & AuthenticationAuthentication: Leverages Spring Security with Basic Auth for secure user authentication.
Authorization: Implements role-based access control with two roles: CUSTOMER and ADMIN.
Password Hashing: Passwords are securely hashed using BCrypt, ensuring they are never stored in plain text.

 User ManagementRegistration: Public endpoint for new users to sign up with their email and a secure password.
Default Role: New users are automatically assigned the CUSTOMER role.
Access Control: Private endpoints are protected, accessible only to authenticated users.

 Video ManagementVideo Catalog: Stores and manages video details, including Title, Director, Genre, and Availability Status.
Public Browsing: Anyone can browse the full list of available videos without authentication.
ADMIN Privileges: Only ADMIN users can create, update, or delete videos.

 API EndpointsThe API follows a clean, RESTful structure for intuitive interaction.Endpoint
HTTP Method
Description
Access
/api/register
POST
Registers a new user
Public
/api/videos
GET
Fetches a list of all videos
Public
/api/videos
POST
Creates a new video
ADMIN Only
/api/videos/{id}
PUT
Updates an existing video
ADMIN Only
/api/videos/{id}
DELETE
Deletes a video
ADMIN Only

 Tech StackFramework: Spring Boot
Security: Spring Security
Database: MySQL (default for production)
H2 (in-memory for development/testing)

ORM: Spring Data JPA
Build Tool: Maven
Utility: Lombok (to reduce boilerplate code)

 Getting StartedFollow these steps to set up and run the RentVideo API locally.PrerequisitesJava 11+ (or higher)
Maven (for dependency management)
MySQL (optional, for production)
IDE (e.g., IntelliJ IDEA, Eclipse) or terminal for running the app

InstallationClone the Repository:bash

git clone https://github.com/SaiManohar-007/Video-Rental-Spring-Boot.git
cd Video-Rental-Spring-Boot

Configure the Database:H2 Database (recommended for local development):No setup required! The app uses an in-memory H2 database by default.

MySQL (for production):Update the src/main/resources/application.properties file with your MySQL credentials:properties

spring.datasource.url=jdbc:mysql://localhost:3306/rentvideo
spring.datasource.username=your-username
spring.datasource.password=your-password

Run the Application:bash

./mvnw spring-boot:run

Alternatively, use your IDE's built-in run feature (e.g., IntelliJ IDEA).
Access the API:
The API will be available at http://localhost:8080.

 UsageRegister a User: Send a POST request to /api/register with an email and password to create a new user.
Browse Videos: Access /api/videos (GET) to view the video catalog.
Admin Actions: Authenticate as an ADMIN user to create, update, or delete videos via the respective endpoints.

 ContributingContributions are welcome! To contribute:Fork the repository.
Create a new branch (git checkout -b feature/your-feature).
Commit your changes (git commit -m 'Add your feature').
Push to the branch (git push origin feature/your-feature).
Open a Pull Request.

 LicenseThis project is licensed under the MIT License. See the LICENSE file for details. ContactFor questions or feedback, reach out via GitHub Issues or connect with the maintainer at [your-email@example.com (mailto:your-email@example.com)].<p align="center">
  <strong>Happy Renting! </strong>
</p>


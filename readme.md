# SCM 2.0 - Contact Management System

## Project Overview
SCM 2.0 is a Spring Boot-based Contact Management System (CMS) designed to provide a user-friendly interface for managing personal contacts. It enables users to register, log in, and maintain a list of contacts, which can include details like name, email, phone number, and profile picture. Additionally, SCM 2.0 provides functionality for searching, adding, updating, and deleting contacts, as well as providing an API for retrieving contact information.

## Features
- **User Authentication**: Secure user authentication using Spring Security.
- **User Registration and Profile Management**: Users can register, log in, and manage their profiles.
- **Contact Management**: 
  - Add new contacts
  - View a list of contacts with pagination
  - Search for contacts by name, email, or phone number
  - Edit and delete existing contacts
- **Contact Image Upload**: Users can upload profile pictures for their contacts, with Cloudinary integration for storing images.
- **REST API**: Provides endpoints for retrieving contact details via API.
- **Custom Flash Messages**: User feedback is provided via custom flash messages for actions like registration, adding contacts, etc.

## Technologies Used
- **Backend**: Spring Boot, Spring Security, JPA (Hibernate)
- **Frontend**: Thymeleaf
- **Database**: MySQL
- **Image Upload**: Cloudinary
- **Validation**: JSR-303 (via Hibernate Validator)
- **Logging**: SLF4J with Logback

## REST API Endpoints
Here is a list of all the endpoints for smc 2.0 application:

## User Endpoints

GET /user/dashboard - User dashboard page.
GET /user/profile - User profile page.

## Contact Management Endpoints
GET /user/contacts/add - View add contact page.
POST /user/contacts/add - Add a new contact.
GET /user/contacts - View all contacts with pagination.
GET /user/contacts/search - Search for contacts.
DELETE /user/contacts/delete/{contactId} - Delete a contact by ID.
GET /user/contacts/view/{contactId} - View contact update page by ID.
POST /user/contacts/update/{contactId} - Update an existing contact by ID.

## Public Pages
GET /home - Home page.
GET /about - About page.
GET /services - Services page.
GET /contact - Contact page.

## Authentication Endpoints
GET /login - Login page.
GET /register - Registration page.
POST /do-register - Process registration.
API Endpoints
GET /api/contacts/{contactId} - Retrieve contact details by ID.

## Project Structure
```plaintext
src
├── main
│   ├── java
│   │   └── com
│   │       └── scm
│   │           ├── controllers   // Controllers for handling user requests
│   │           ├── entities      // JPA entities representing data models
│   │           ├── forms         // Form objects for request validation
│   │           ├── helpers       // Utility classes for common functionalities
│   │           ├── services      // Service layer for business logic
│   └── resources
│       ├── templates             // Thymeleaf templates for frontend pages
│       ├── application.properties // Application configurations
└── test
    └── java
        └── com
            └── scm
                └── tests         // Unit tests for the application




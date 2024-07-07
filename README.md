# To-do_app_scalable_backend_system

# Task Manager Web Application

This repository contains a Flask-based web application for managing tasks. Users can create, view, update, and delete tasks, with authentication and authorization mechanisms in place.

## Overview

The Task Manager Web Application is built using Flask, a lightweight Python web framework. It utilizes MySQL for data storage and includes features such as user authentication, task management, and API endpoints for CRUD operations on tasks.

## Features

- User Authentication: Users can sign up, log in, and log out securely using OAuth for authentication. Passwords are hashed using bcrypt before being stored in the database.
- Task Management: Authenticated users can create, view, update, and delete tasks. Tasks are associated with the user who created them.
- Session Management: User sessions are maintained using Flask's session management system, allowing users to stay logged in across multiple requests.
- RESTful API: The application provides RESTful API endpoints for interacting with tasks, allowing integration with other services or front-end applications.
- Admin Portal: An admin portal is available for administrators to manage user accounts. Administrators can view user accounts from the portal.
- Caching: Redis is used as a caching layer to improve performance by caching frequently accessed data.
- Load Balancing: NGINX is configured as a load balancer to distribute incoming network traffic across multiple servers, improving responsiveness and availability of the application.
- Distributed Caching: Redis is configured for distributed caching, allowing for the storage and retrieval of cache data across multiple instances of application.

## Prerequisites

Before running the application, ensure you have the following installed:

- Python 3.x
- MySQL server
- Redis server
- NGINX

## Getting Started

1. Clone the repository to your local machine:

   ```bash
   git clone https://github.com/DheerajKommineni/449_To-do_app_scalable_backend_system
   ```

2. Navigate to the project directory:

   ```bash
   cd 449_To-do_app_scalable_backend_system
   ```

3. Install the required Python packages:

   ```bash
   pip install -r requirements.txt
   ```

4. Set up the MySQL database:

   - Create a MySQL database named `todo_db`.
   - Update the database connection details in `app.py` if necessary.

5. Set up the Redis server:

   - Ensure Redis server is running on `localhost` with default port `6379`.

6. Configure NGINX as a load balancer:

   - Update NGINX configuration to distribute traffic across multiple instances of the Flask application.
   - Ensure NGINX is configured to forward requests to the appropriate Flask instances.

7. Run the application:

   ```bash
   python app.py
   ```

8. Access the application in your web browser at `http://localhost:5001`.

## Usage

- Register a new account or log in with existing credentials.
- Add, update, or delete tasks from the dashboard.
- Log out when finished.

## Admin Portal

- Access the admin portal by logging in with the admin credentials:
  - Email: admin@gmail.com
  - Password: Admin@123
- Manage user accounts and view user details from the admin dashboard.

## Contributing

Contributions are welcome! Feel free to open issues or pull requests for any improvements or feature additions.

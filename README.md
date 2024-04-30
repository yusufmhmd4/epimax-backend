# Task Management System

This is a simple Task Management System built with Node.js, Express, SQLite, and JWT authentication.

## Features

- User registration and login with JWT authentication.
- Create, read, update, and delete tasks.
- Retrieve tasks assigned to specific users.
- Retrieve all users and tasks.
- Admin functionality to delete users.

## Setup

1. **Clone the repository**

   ```bash
   git clone https://github.com/yusufmhmd4/epimax-backend
   ```
     
2. **Install dependencies**

   ```bash
   npm install
   ```
     
3. **Run the server**

   ```bash
   node index.js
   ```

#
**Render Deployement** : https://epimax-backend.onrender.com/login
#


## API Endpoints
     
## User Login

- **URL:** `/login`
- **Method:** `POST`
- **Request Body:** JSON

  ```json
  {
    "username":"yusufmhmd",
    "password":"yusufmhmd",
    "isAdmin":true
  }
  ```

## Register a New User

- **URL:** `/register`
- **Method:** `POST`
- **Request Body:** JSON

  ```json
  {
    "name": "Yusuf Baba",
    "username": "yusuf",
    "password": "yusuf"
  }
  ```

## Create a New Task

- **URL:** `/tasks`
- **Method:** `POST`
- **Request Body:** JSON

  ```json
  {
    "title": "Task Title",
    "description": "Task Description",
    "status": "Pending",
    "assignedId": 1
  }
  ```

## Retrieve All Users

- **URL:** `/users`
- **Method:** `GET`
- **Authentication:** JWT Token required

## Delete a User (Admin Only)

- **URL:** `/users/:userId`
- **Method:** `DELETE`
- **Authentication:** JWT Token required
- **Note:** Admin only can remove users.

## Retrieve All Tasks

- **URL:** `/tasks`
- **Method:** `GET`
- **Authentication:** JWT Token required

## Retrieve Tasks Assigned to a Specific User

- **URL:** `/users/tasks`
- **Method:** `GET`
- **Authentication:** JWT Token required

## Retrieve a Specific Task

- **URL:** `/tasks/:taskId`
- **Method:** `GET`
- **Authentication:** JWT Token required

## Update a Specific Task

- **URL:** `/tasks/:taskId`
- **Method:** `PUT`
- **Request Body:** JSON

  ```json
  {
    "title": "Updated Task Title",
    "description": "Updated Task Description",
    "status": "Completed"
  }
  ```

- **Authentication:** JWT Token required

## Delete a Specific Task

- **URL:** `/tasks/:taskId`
- **Method:** `DELETE`
- **Authentication:** JWT Token required

## Technologies Used

- **Node.js**
- **Express.js**
- **SQLite**
- **JWT Authentication**

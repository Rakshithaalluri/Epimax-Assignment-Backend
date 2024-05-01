**TODO TASKS API**
This is a RESTful API built with Express.js for managing todo tasks. It provides endpoints for user authentication, task management (CRUD operations), and task assignment.

**Prerequisites**
Node.js installed on your machine
SQLite database driver for Node.js

**Setup**
Clone this repository to your local machine.
Install dependencies by running npm install.
Run the server using npm start.

**Usage**
Sign Up
URL: /signup
Method: POST
Request Body:
{
  "username": "your_username",
  "password_hash": "your_password"
}

**Login**
URL: /login
Method: POST
Request Body:
{
  "username": "your_username",
  "password_hash": "your_password"
}
Response:
{
  "jwtToken": "your_generated_jwt_token"
}

**Create Task**
URL: /tasks
Method: POST
Request Body:
{
  "title": "Task Title",
  "description": "Task Description",
  "status": "Task Status",
  "assignee_id": assignee_id
}
Note: Ensure you include the JWT token in the Authorization header as a Bearer token.

**Get All Tasks**
URL: /tasks
Method: GET
Request Header:
Authorization: Bearer your_jwt_token

**Get Task by ID**
URL: /tasks/:id
Method: GET
Request Header:
Authorization: Bearer your_jwt_token

**Update Task**
URL: /tasks/:id
Method: PUT
Request Header:
Authorization: Bearer your_jwt_token
Request Body:
{
  "title": "Updated Task Title",
  "description": "Updated Task Description",
  "status": "Updated Task Status",
  "assignee_id": updated_assignee_id
}

**Delete Task**
URL: /tasks/:id
Method: DELETE
Request Header:
Authorization: Bearer your_jwt_token


**Authentication**
JWT (JSON Web Tokens) are used for authentication. Tokens should be included in the Authorization header as a Bearer token.

**Database**
SQLite is used as the database. Ensure the database file (user_tasks.db) is in the project directory.

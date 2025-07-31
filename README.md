Todo List API

This project is a simple Todo List backend API built using Node.js and Express framework, with MongoDB as the database. 
It allows users to create, read, update, and delete tasks. A bonus feature of the project is the ability to classify tasks by difficulty level: easy, medium, or hard. 
If no difficulty level is specified when creating a task, it defaults to medium.

==================================================================================================================================================

The API exposes several routes to manage tasks:

 * POST /api/tasks/ creates a new task.

 * GET /api/tasks/ retrieves all tasks.

 * GET /api/tasks/:id retrieves a specific task by its ID.

 * PATCH /api/tasks/:id updates a task by its ID.

 * DELETE /api/tasks/:id deletes a task by its ID.

Each task includes fields such as title, description, and difficulty.

To set up the project locally, you need to have Node.js installed, as well as access to a MongoDB database. 
First, clone the repository from https://github.com/DitoT/TodoList and navigate into the project folder. Run 
 'npm install'
to install all necessary dependencies. 
Then, create a .env file in the root directory and add your MongoDB connection string as MONGO_URI along with the port number, for example, PORT=5000.

To start the server, 
run 'npm start' for production or 'npm run dev '
to start the development server with hot reload. The API will then be available at 'http://localhost:5000/api/tasks'

==================================================================================================================================================

Deployment Instructions

To deploy this backend on a cloud platform such as Render, follow these steps:

1)Push your code to a GitHub repository.

2)On Render, create a new Web Service and connect it to your GitHub repository.

3)Set the build command to npm install and the start command to node src/app.js (adjust the path if your entry file differs).

4)Add environment variables on Render for MONGO_URI with your MongoDB connection string and PORT (usually 5000).

5)Deploy the service. Once deployed, your API will be accessible via a Render-generated URL.

6)Test the deployed API endpoints using tools like Postman or curl.

==================================================================================================================================================

Usage Examples

To create a new task, send a 'POST' request to '/api/tasks' with a JSON body like:

{
  "title": "Finish homework",
  "description": "Math and Science assignments",
  "difficulty": "hard"
}

To retrieve all tasks, send a 'GE'T request to /api/tasks.

To update a task, send a 'PATCH' request to /api/tasks/:id with the fields you want to update.

To delete a task, send a 'DELETE' request to /api/tasks/:id.

==================================================================================================================================================

Installations

npm init -y
npm install express mongoose dotenv

npm install -g nodemon
  or
npm install --save-dev nodemon

Edit 'package.json' and add:
"scripts": {
  "start": "node src/app.js",
  "dev": "nodemon src/app.js"
}

create .env folder:
MONGO_URI=your_mongodb_connection_string
PORT=5000

For production: npm start
For development: npm run dev



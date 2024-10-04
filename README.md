# To-Do Application
A simple full-stack To-Do application with the following features:

* Add, view, and delete tasks from a list.
* Backend API built with Node.js and Express.
* MongoDB as the database to persist tasks.
* React frontend to interact with the API.

  ![image](https://github.com/user-attachments/assets/71ccd83c-0dd5-4dec-a1d7-1a428b8d18c8)

## Features
###  Frontend (React):
* Add tasks.
* Display a list of tasks.
* Delete tasks.
###  Backend (Node.js and Express):
* GET /tasks: Retrieve all tasks.
* POST /tasks: Add a new task.
* DELETE /tasks/:id: Delete a task by ID.

## Technologies Used
* Frontend: React.js, Axios for API calls.
* Backend: Node.js, Express.js, Mongoose (for MongoDB integration).
* Database: MongoDB (MongoDB Atlas or local MongoDB).

## Installation and Setup Instructions

### Clone the Repository
 
cd C:\Users\Dell\Downloads\MERN-TO-DO-APP-main
git init
git add .
git commit -m "Your commit message here"
git remote add origin https://github.com/atulanurag8544/To-Do-App.git
git fetch origin
git merge origin/main --allow-unrelated-histories  
git push -u origin main  

   
 ## 2. Install Dependencies
 
   ## Backend (Node.js and Express):

### Navigate to the backend folder:


cd api

npm install

## Frontend (React):

### Navigate to the frontend folder:


cd ../todo-app

npm install

 ###  3. Configure MongoDB
If using MongoDB Atlas, ensure your connection URI is correctly configured in the backend:

### Open backend/server.js:

Replace the MongoDB connection URI with your own:


mongoose.connect('your-mongodb-uri-here', { useNewUrlParser: true, useUnifiedTopology: true })

Ensure the IP of the machine you are working on is whitelisted in MongoDB Atlas.

### 4. Running the Application
  ## Backend (Node.js/Express)

### Start the backend server:

cd api

node server.js

The backend will run on http://localhost:5000.

## Frontend (React)

### Start the frontend:


cd todo-app

npm start

The frontend will run on http://localhost:3000.

### 5. Proxy Configuration
   Ensure the frontend is correctly communicating with the backend by setting up a proxy. In frontend/package.json, add:


"proxy": "http://localhost:5000"
This allows React to send requests to your Node.js server running on port 5000.

### Usage
* Navigate to the frontend at http://localhost:3000.
* Use the form to add a new task.
* View the tasks listed below the form.
* Click the delete button to remove a task.
## API Endpoints
### GET /tasks:
 Retrieve all tasks.
### POST /tasks:
 Add a new task.
Request Body: { "name": "Task name" }
### DELETE /tasks/
: Delete a task by its ID.



## Author
Atul Anurag

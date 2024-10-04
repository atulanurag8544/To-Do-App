To-Do Application
A simple full-stack To-Do application with the following features:

Add, view, and delete tasks from a list.
Backend API built with Node.js and Express.
MongoDB as the database to persist tasks.
React frontend to interact with the API.
Features
Frontend (React):
Add tasks.
Display a list of tasks.
Delete tasks.
Backend (Node.js and Express):
GET /tasks: Retrieve all tasks.
POST /tasks: Add a new task.
DELETE /tasks/:id: Delete a task by ID.
MongoDB:
Tasks are stored in MongoDB for persistent storage.
Technologies Used
Frontend: React.js, Axios for API calls.
Backend: Node.js, Express.js, Mongoose (for MongoDB integration).
Database: MongoDB (MongoDB Atlas or local MongoDB).
Installation and Setup Instructions

1. Clone the Repository
   bash
   Copy code
   git clone https://github.com/your-username/todo-app.git
   cd todo-app
2. Install Dependencies
   Backend (Node.js and Express):

Navigate to the backend folder:

bash
Copy code
cd backend
npm install
Frontend (React):

Navigate to the frontend folder:

bash
Copy code
cd ../frontend
npm install 3. Configure MongoDB
If using MongoDB Atlas, ensure your connection URI is correctly configured in the backend:

Open backend/server.js:

Replace the MongoDB connection URI with your own:

javascript
Copy code
mongoose.connect('your-mongodb-uri-here', { useNewUrlParser: true, useUnifiedTopology: true })
Ensure the IP of the machine you are working on is whitelisted in MongoDB Atlas.

4. Running the Application
   Backend (Node.js/Express)

Start the backend server:

bash
Copy code
cd backend
node server.js
The backend will run on http://localhost:5000.

Frontend (React)

Start the frontend:

bash
Copy code
cd frontend
npm start
The frontend will run on http://localhost:3000.

5. Proxy Configuration
   Ensure the frontend is correctly communicating with the backend by setting up a proxy. In frontend/package.json, add:

json
Copy code
"proxy": "http://localhost:5000"
This allows React to send requests to your Node.js server running on port 5000.

Usage
Navigate to the frontend at http://localhost:3000.
Use the form to add a new task.
View the tasks listed below the form.
Click the delete button to remove a task.
API Endpoints
GET /tasks: Retrieve all tasks.
POST /tasks: Add a new task.
Request Body: { "name": "Task name" }
DELETE /tasks/
: Delete a task by its ID.
Folder Structure
bash
Copy code
todo-app
│
├── backend
│ ├── server.js # Express server setup
│ └── package.json # Backend dependencies
│
└── frontend
├── src
│ ├── App.js # Main React component
│ ├── TaskForm.js # Task input form component
│ └── TaskList.js # Task list component
└── package.json # Frontend dependencies
Additional Notes
Ensure MongoDB is running (or the connection to MongoDB Atlas is properly configured).
Modify the MongoDB connection URI as needed in server.js.
Use axios in the frontend for handling API requests to the backend.
License
This project is licensed under the MIT License.

Author
Your Name

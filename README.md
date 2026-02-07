# TaskBoard – Multi-Page To-Do Web Application

## Overview
TaskBoard is a simple multi-page to-do web application developed using **Node.js** and **Express**.  
The goal of this project is to demonstrate a working client–server architecture with a RESTful API that supports **GET**, **POST**, and **DELETE** requests, as required for CPS630 Assignment 1.

The application allows users to view a list of tasks, add new tasks, and delete existing tasks through a browser interface. All data is stored as a JSON object on the server.

---

## Technologies Used
- Node.js
- Express.js
- HTML5
- CSS3
- JavaScript (Fetch API)

---

## Features
- Express server implemented in `server.js`
- Server-side JSON object used to store task data
- Three distinct HTML pages
- REST API with proper HTTP methods and status codes
- Client-side interaction using JavaScript `fetch()`
- Static files served using Express middleware
- User feedback messages for actions (add/delete)

---

## Application Pages

### Home Page (`/`)
- Introduction to the application
- Navigation to other pages

### Tasks Page (`/tasks`)
- Displays the list of tasks (GET request)
- Allows users to add a new task (POST request)
- Allows users to delete an existing task (DELETE request)
- Displays status messages confirming actions

### About Page (`/about`)
- Describes the application
- Lists available REST API endpoints

---

## REST API

### GET – Retrieve All Tasks

**Response:**
- Status: `200 OK`
- Returns a JSON object containing the list of tasks

---

### POST – Add a Task
**Request Body (JSON):**
```json
{
  "title": "Task title"
}
```
### Delete a Task
DELETE /api/tasks/:id


### Responses
- `200 OK` – Task successfully deleted
- `400 Bad Request` – Invalid task ID
- `404 Not Found` – Task does not exist


### Project Structure
```text
project-root/
├── server.js
├── package.json
└── public/
    ├── index.html
    ├── tasks.html
    ├── about.html
    └── css/
        └── styles.css
```

### How to Run the Application
### Prerequisites
Node.js (version 16 or later recommended)
npm (included with Node.js)

### Steps

- Clone the repository:
git clone <repository-url>

- Navigate to the project directory:
cd project-root

- Install dependencies:
npm install

- Start the server:
npm start

- Open a web browser and visit:
http://localhost:3000

### How to Use
- Open the **Tasks** page.
- Enter a task title and click **Add**.
- The task list updates immediately.
- Click **Delete** to remove a task.
- Status messages appear on the page to confirm each action.

### Notes
Task data is stored in memory using a JSON object on the server.
Restarting the server will reset the task list.

This application is intended for educational purposes.

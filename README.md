# Student Management API

This is a small Node.js and Express project for managing a list of students.
I used an array for the data, so there is no database in this project. Any new
students or changes will be lost when the server is stopped.

## Running the project

Open a terminal in this folder and run:

```bash
npm install
npm start
```

The server starts at `http://localhost:3000`.

## Files

- `app.js` starts the server and connects the routes.
- `routes/studentRoutes.js` contains the student CRUD operations.
- `data/students.js` contains the starting student data.
- `middleware/logger.js` prints each request in the terminal.

## Routes

| Method | URL | What it does |
| --- | --- | --- |
| GET | `/students` | Shows all students |
| GET | `/students/:id` | Shows one student |
| POST | `/students` | Adds a student |
| PUT | `/students/:id` | Changes a student |
| DELETE | `/students/:id` | Removes a student |

For POST and PUT requests, send JSON like this:

```json
{
  "name": "Rohit",
  "course": "MCA"
}
```

The `name` and `course` fields are required. The API returns `400` if either

field is missing and `404` if the student ID cannot be found.

I tested the routes using Postman.

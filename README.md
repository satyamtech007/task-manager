# Task Manager & Note Files Web App

A clean, responsive, dark-mode full-stack web application built to match and elevate the localhost task manager interface.

## ✨ Features

- **Exact Visual Design**: Sleek dark aesthetic with rounded input fields, deep charcoal card containers, and vibrant blue action buttons matching the layout.
- **Auto `.txt` Naming**: Automatically saves files with `.txt` extensions (mimicking the Node.js/Express `fs.writeFile` tutorial behavior).
- **Interactive Modals**:
  - **Read More**: View full task details, timestamp, character count.
  - **Quick Actions**: Copy content to clipboard, edit filename and details, download directly as a `.txt` file, or delete tasks.
- **Search & Filter**: Real-time instant search across file names and details.
- **Sorting Options**: Default (screenshot arrangement), Newest First, or Alphabetical (A-Z).
- **Persistent Storage**: Tasks are saved as real `.txt` files in a `tasks/` folder on the server using Node's `fs` module.
- **Reset to Demo Tasks**: Easily restore the original tasks (`.txt`, `test1.txt`, `something.txt`).

## 🚀 How to Run

1. Install dependencies: `npm install`
2. Start the server: `npm start`
3. Open http://localhost:3000 in your browser

## 🛠️ Backend Routes (Express + fs)

- `POST /tasks` reads `title` and `description` from `req.body` and saves them as a `.txt` file with `fs.writeFile`
- `GET /tasks` lists all saved tasks with `fs.readdir`
- `GET /tasks/:name` reads one full task with `fs.readFile` using `req.params.name`

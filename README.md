# 3-Tier E-Commerce Application – Local Deployment Guide

This project is a 3-tier e-commerce application built with:

- **Frontend:** React
- **Backend:** Node.js + Express
- **Database:** MySQL

This guide explains how to deploy and run the application locally for development and testing.

---

## 📁 Project Structure

project-root/
│
├── frontend/ # React application
├── backend/ # Node.js/Express API
└── database/ # MySQL (installed locally)

---

## ✅ Prerequisites

Ensure the following are installed:

- Node.js (v16 or higher)
- npm
- MySQL Server
- Git

Verify installation:

````bash
node -v
npm -v
mysql --version


---

## ✅ Prerequisites

Ensure the following are installed:

- Node.js (v16 or higher)
- npm
- MySQL Server
- Git

Verify installation:

```bash
node -v
npm -v
mysql --version

## Step 1: Clone the Repository

```bash
git clone <repository-url>
cd <project-folder>

## Step 2: Set Up MySQL Database

```bash
sudo systemctl start mysql


### Windows
Start MySQL from Services or MySQL Workbench.

Create the Database

```bash
Login to MySQL:
mysql -u root -p
Create the database:
CREATE DATABASE ecommerce;
Exit MySQL:
EXIT;


## Step 3: Run the Backend (API Server)

Navigate to the backend directory:

```bash
cd backend
#Install Dependencies
npm install

Create Environment Variables

Inside the backend folder, create a .env file:

```bash
PORT=5000
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=your_mysql_password
DB_NAME=ecommerce


Ensure credentials match your MySQL setup.

Start the Backend Server
```bash
npm start


Or (if using nodemon):

```bash
npm run dev


Backend will run at:

```bash
http://localhost:5000

##🎨 Step 4: Run the Frontend (React App)

Open a new terminal and navigate to the frontend folder:

```bash
cd frontend
# Install Dependencies
npm install

Configure API URL

Create a .env file inside the frontend folder:

```bash
REACT_APP_API_URL=http://localhost:5000

Start the React Development Server
```bash
npm start


Frontend will run at:

```bash
http://localhost:3000

 How It Works Locally

React runs on port 3000

Node.js backend runs on port 5000

Backend connects to local MySQL

Frontend sends API requests to backend

Backend retrieves data from MySQL and responds

🛑 Stopping the Application

To stop frontend or backend:

```bash
Ctrl + C


Ensure MySQL remains running if restarting the backend.    change this to markdown
````

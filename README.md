Blog App

A full-stack Blog Application built with:

Nginx (Frontend)

Flask (Backend API)

MySQL (Database)


Docker & Docker Compose

 Project Overview

This project is a containerized blog platform where users can:

Create blog posts

View blog posts

Store posts in a MySQL database

Run the entire stack using Docker Compose

The application uses a custom Docker network (blog-net) and a persistent MySQL volume (mysql-data).


 Architecture
Client (Browser)
        ↓
     Nginx
        ↓
     Flask API
        ↓
     MySQL Database
     

Project Structure
project3/
│
├── docker-compose.yml
├── README.md
├── .gitignore
│
├── frontend/
│   ├── Dockerfile
│   └── index.html
│
└── backend/
    ├── Dockerfile
    ├── app.py
    └── requirements.txt
    

Technologies Used

Python 3

Flask

MySQL 8

Nginx

Docker

Docker Compose

🐳 How to Run the Project
1️⃣ Clone the Repository
git clone https://github.com/ucosuji/project3.git
cd project3

2️⃣ Build and Start Containers
docker-compose up --build

3️⃣ Access the Application

Frontend:

http://localhost:88


Backend API:

http://localhost:5000


MySQL:

localhost:3306

Environment Variables

The backend connects to MySQL using:

MYSQL_HOST=db
MYSQL_USER=bloguser
MYSQL_PASSWORD=blogpassword
MYSQL_DB=blogdb


These are defined in docker-compose.yml.

📦 Docker Configuration
Network

blog-net (bridge network)

Volume

mysql-data (persistent database storage)



Author

Uchechukwu
GitHub: https://github.com/ucosuji

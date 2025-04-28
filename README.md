# Three-Tier Application Deployment using Docker Compose


![Architecture](assets/Infra.gif)

This repository showcases the deployment of a three-tier application using Docker Compose. The application consists of a MySQL database, a Node.js backend, and a React.js frontend.


# Dockerizing and Deploying Three-Tier Full Stack Applications
- Deployed multi-tier full-stack applications using Docker and Docker Compose, ensuring seamless integration and scalability.
- Configured custom networks and volumes for efficient container communication and data persistence across Node.js and React.js applications.
- Managed MySQL databases within Docker containers, ensuring data integrity and availability through effective volume management.


## Prerequisites

Before you begin, make sure you have the following installed:

- [Docker](https://www.docker.com/get-started)
- [Docker Compose](https://docs.docker.com/compose/install/)

## Project Structure

- **frontend**: Dockerfile and related files for the React.js frontend.
- **backend**: Dockerfile and related files for the Node.js backend.
- **docker-compose.yml**: Docker Compose configuration file.
- **student-teacher-app**: Code for the frontend application.
- **backend**: Code for the backend application.

## Deployment Steps

1. **Clone the Repository:**
   ```bash
   git clone <repository-url>
   cd <repository-directory>
   ```

2. **Build and Run Docker Containers:**
    Use Docker Compose to build and run all containers:
    ```bash
    docker-compose up -d
    ```

3. **Access the Application:**

    Open your favourite browser and visit http://localhost:80. Explore the MERN stack application!

### MYSQL Configuration
``` bash
CREATE DATABASE school;
USE school;
CREATE TABLE student (id INT AUTO_INCREMENT PRIMARY KEY, name varchar(40), roll_number int, class varchar(16));
CREATE TABLE teacher (id INT AUTO_INCREMENT PRIMARY KEY, name varchar(40), subject varchar(40), class varchar(16));
```
## Data Persistence
    Data persistence is ensured by using Docker volumes. If the MySQL container is deleted, data remains available and is automatically added to a new Docker container by providing the same Docker volume.

    Feel free to explore and modify the Docker Compose file and related files to enhance your understanding of containerization and deployment using Docker Compose! Happy coding! 🚀


npm install express mysql cors nodemon

### MYSQL Configuration
``` bash
CREATE DATABASE school;

USE school;

CREATE TABLE student (id INT AUTO_INCREMENT PRIMARY KEY, name varchar(40), roll_number int, class varchar(16));

CREATE TABLE teacher (id INT AUTO_INCREMENT PRIMARY KEY, name varchar(40), subject varchar(40), class varchar(16));
```
### Backend-

``` bash
Install nodejs npm install dotenv Modify the .env and do the changes for database

npm install -g pm2

pm2 start npm --name backend -- start
```
Frontend Modify the .env file and update the backend api endpoint

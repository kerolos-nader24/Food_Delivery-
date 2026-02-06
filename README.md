FOOD-DELIVERY 🍔🚀

FOOD-DELIVERY is a modern full-stack food delivery application. It consists of three main components: the Backend built with Node.js and Express, the Frontend built with React, and the Admin Panel also built with React. The project is fully containerized using Docker and Docker Compose, and it includes a GitHub Actions workflow to automate building, testing, and verification of all services. 🐳⚙️

Project Structure 📂

The project is organized into separate folders for each service:

.github/workflows/main.yml – GitHub Actions workflow

backend/ – Backend server with Node.js + Express

frontend/ – Frontend application built with React

admin/ – Admin panel built with React

docker-compose.yml – Runs all services together

Setting Up and Running the Project 🛠️

To start the project, you first need to build Docker images for each component. For the backend, frontend, and admin panel, you build the images so each service runs in its own container. After building, you can start all services together using Docker Compose, which ensures a consistent environment and allows all components to communicate with each other properly.

To build the Docker images, you would run Docker build commands for the backend, frontend, and admin panel.

To start all services, you run Docker Compose, which launches the backend at http://localhost:5000, the frontend at http://localhost:3000, and the admin panel at http://localhost:8080.

After testing, you can stop all services by stopping Docker Compose. ✅

Using Docker Hub Images 🌐

After successfully building and testing locally, the Docker images can be pushed to Docker Hub under the username kerolos024. Once uploaded, Docker Compose can pull these images directly from Docker Hub without requiring a local build, making it easy for anyone to run the application anywhere.

Backend image: kerolos024/food-delivery-backend
 🐍

Frontend image: kerolos024/food-delivery-frontend
 ⚛️

Admin image: kerolos024/food-delivery-admin
 🖥️

To test the application using Docker Hub images, you pull the images from Docker Hub and then run Docker Compose, ensuring that the environment is identical across all systems.

GitHub Actions Workflow ⚙️

The project includes a GitHub Actions workflow located in .github/workflows/main.yml. This workflow automates:

Building Docker images for backend, frontend, and admin panel

Running Docker Compose to launch all services

Verifying that the backend service responds correctly

This ensures that any updates to the project are tested automatically, reducing the chance of errors reaching production.

Notes and Recommendations 📌

The project runs entirely using Docker Compose, so no local Node.js installation is required.

Environment variables can be customized using .env files.

It is recommended to test all services locally first before pushing images to Docker Hub to ensure everything works as expected.

You can add additional services or extend the workflow to automatically push Docker images after successful testing.

Summary 🎯

FOOD-DELIVERY is a professional full-stack Dockerized project with automated CI/CD workflow using GitHub Actions. It is easy to set up, easy to run, and ready for both development and production environments. Feedback, contributions, and improvements are highly welcome
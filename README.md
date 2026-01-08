HTML CI/CD Pipeline using Docker & GitHub Actions
📌 Project Overview
This project demonstrates a complete CI/CD pipeline for a simple static HTML application using Docker and GitHub Actions.
Whenever code is pushed to the repository, the pipeline automatically builds, containerizes, and deploys the application.
🛠️ Tech Stack
HTML – Static web application
Docker – Containerization
GitHub Actions – CI/CD automation
Nginx – Web server inside container
🔁 CI/CD Workflow
The pipeline is triggered automatically on every push to the main branch.
Workflow Steps:
Checkout source code from GitHub
Build Docker image using Dockerfile
Run Docker container to deploy the application
📂 Project Structure
Copy code

hyml-cicd/
├── index.html        # Static HTML file
├── Dockerfile        # Docker configuration
└── .github/
    └── workflows/
        └── ci-cd.yml # GitHub Actions CI/CD pipeline
🐳 Dockerfile
Dockerfile
FROM nginx:alpine
COPY . /usr/share/nginx/html
This Dockerfile:
Uses lightweight Nginx image
Copies HTML files into the web server directory
Serves the application on port 80
⚙️ GitHub Actions Pipeline

.github/workflows/ci-cd.yml
Key actions performed:
Builds Docker image
Runs container automatically
🚀 Deployment
Deployment is handled automatically inside the GitHub Actions runner
The application runs in a Docker container after every successful build
This setup demonstrates automated deployment without manual intervention


How to Run Locally
Copy code
Bash
docker build -t html-app .
docker run -d -p 8080:80 html-app

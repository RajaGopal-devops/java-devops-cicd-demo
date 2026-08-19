# Java DevOps & Cloud CI/CD Demo

This repository demonstrates an end-to-end DevOps automation pipeline for a Java Spring Boot microservice using **Jenkins, Docker, Maven, and GitHub**.

## Tech Stack & Tools Used
* **Source Code:** Java / Maven
* **Version Control:** Git & GitHub
* **CI/CD Automation:** Jenkins (Declarative Pipeline)
* **Containerization:** Docker
* **Deployment Target:** Containerized Runtime / Cloud

## Pipeline Workflow
1. **Source Code Checkout:** Pulls latest code from GitHub main branch.
2. **Build & Test:** Compiles Java code and builds `.jar` artifact using Maven (`mvn clean package`).
3. **Containerization:** Packages the application JAR into a lightweight Docker container using `Dockerfile`.
4. **Deployment:** Runs the containerised app serving on port 8080.

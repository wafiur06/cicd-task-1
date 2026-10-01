# Task 1: Automate Code Deployment Using CI/CD Pipeline

## Objective
Set up a Continuous Integration and Continuous Deployment (CI/CD) pipeline to automatically build, test, and deploy a web application using GitHub Actions.

## Tools & Technologies Used
- **Version Control:** Git & GitHub
- **CI/CD:** GitHub Actions
- **Application Environment:** Node.js
- **Containerization:** Docker & DockerHub

## Repository Structure
- `.github/workflows/main.yml`: The GitHub Actions workflow configuration file that defines the CI/CD pipeline.
- `Dockerfile`: Instructions to containerize the Node.js application.
- `package.json`: Application metadata, dependencies, and test scripts.
- `server.js`: A simple Node.js web server used as the sample application.

## Steps Completed
1. **Application Setup:** Created a basic Node.js application with a standard test script.
2. **Containerization:** Wrote a `Dockerfile` to package the app using the `node:18-alpine` base image.
3. **Pipeline Configuration:** Developed a GitHub Actions workflow to trigger automatically on every `push` to the `main` branch.
4. **CI (Continuous Integration):** Configured the pipeline to checkout code, set up the Node.js environment, install dependencies (`npm install`), and run tests (`npm test`).
5. **CD (Continuous Deployment):** Configured the pipeline to securely log in to DockerHub using GitHub Secrets (`DOCKERHUB_USERNAME` and `DOCKERHUB_TOKEN`), build the Docker image, and push it to the DockerHub registry.

## Result
Every commit pushed to the `main` branch successfully triggers the workflow, runs the automated tests, and pushes the latest Docker image to DockerHub without manual intervention.
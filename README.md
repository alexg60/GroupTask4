# 🚀 Automated Java App Deployment with Docker and GitHub Actions

This project demonstrates how to automate the deployment of a Java application to Docker Hub using GitHub Actions. It showcases how Docker helps with containerization, and how GitHub Actions handles continuous integration and delivery (CI/CD).

---

## 📁 Project Structure


---

## 🧰 Use of Docker and GitHub Actions
GitHub Actions
GitHub Actions is used to automate the build and deployment process. A workflow runs every time code is pushed to the main branch. It performs the following steps:

Checks out the repository

Logs in to Docker Hub using credentials stored in GitHub Secrets (DOCKER_USERNAME and DOCKER_PASSWORD)

Builds the Docker image using the Dockerfile

Pushes the image to Docker Hub with a unique tag (is147:<run_number>)

This automation ensures that the application is always up-to-date on Docker Hub with no manual deployment steps.

### 🐳 Docker

Docker is used to **containerize** the Java application. This ensures the app runs consistently on any machine with Docker installed. The Dockerfile:

- Uses the official `openjdk:23` image as a base.
- Copies Java source files into the container.
- Compiles the Java files using `javac`.
- Runs the application using the `java` command.

This allows you to build and run your application using simple Docker commands:

```bash
docker pull your-dockerhub-username/is147:tag
docker run your-dockerhub-username/is147:tag

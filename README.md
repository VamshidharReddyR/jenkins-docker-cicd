# Jenkins Docker CI/CD Pipeline

A production-style CI/CD demonstration project built with Python, Flask, Docker, and Jenkins.

The project demonstrates how source code can be tested, containerized, and validated automatically through a Jenkins CI pipeline.

---

## Architecture

```text
Developer
    |
    | git push
    v
GitHub
    |
    | Jenkins SCM
    v
Jenkins Pipeline
    |
    +----------------------+
    |                      |
    v                      v
Install Dependencies     Run Tests
                           |
                           v
                      JUnit Report
                           |
                           v
                    Build Docker Image
                           |
                           v
                 jenkins-docker-cicd:<BUILD_NUMBER>

# 🚀 Windows-Based DevOps CI/CD Pipeline Using Jenkins

## 📌 Project Overview

This project demonstrates a **CI/CD pipeline built on Windows** to automate source code checkout, code quality checks, WAR packaging, and web application deployment.

The pipeline integrates Git, GitHub, Jenkins, Apache Ant, Checkstyle, and Apache Tomcat to demonstrate an end-to-end DevOps workflow.

**Project Status:** Successfully tested locally, including application deployment to Tomcat.

## 🏗️ Architecture

```text
        Developer
            |
            v
       GitHub Repository
            |
            v
    Jenkins - FirstJob
      Source Checkout
         Poll SCM
            |
            v
    Jenkins - SecondJob
     Apache Ant + Checkstyle
       Code Quality Check
            |
            v
     Jenkins - ThirdJob
        Build WAR File
            |
            v
      Apache Tomcat
            |
            v
     Running Web Application
```
Architecture Diagram:
<img width="1536" height="1024" alt="DevOps CI_CD Pipeline Architecture" src="https://github.com/user-attachments/assets/1d6e4acd-373d-4ea9-acf8-17a80aaeadff" />


## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Windows | Development and build environment |
| Git | Version control |
| GitHub | Source code repository |
| Jenkins | CI/CD automation |
| Java JDK 21 | Java development environment |
| Apache Ant | Build automation |
| Checkstyle | Java code quality checks |
| Apache Tomcat 11 | Web application server |
| WAR | Web application packaging format |

## ⚙️ Pipeline Workflow

### 1. FirstJob — Source Code Checkout
- Connects Jenkins to the GitHub repository.
- Checks out the source code.
- Uses Poll SCM to check for repository changes.

### 2. SecondJob — Code Quality Check
- Uses Apache Ant to execute the configured `checkstyle` target.
- Performs the configured code quality checks.
- Runs as the next stage in the Jenkins job chain.

### 3. ThirdJob — Build and Deployment
- Uses Apache Ant to execute the `war` target.
- Packages the web application into a WAR file.
- Deploys the WAR file to Apache Tomcat using the Jenkins Deploy to Container plugin.
- Verifies that the application is accessible in the browser.

## 🎯 Key Learning Outcomes

- Configuring Jenkins jobs and build triggers.
- Integrating GitHub with Jenkins.
- Automating builds with Apache Ant.
- Integrating Checkstyle into a build workflow.
- Packaging Java web applications as WAR files.
- Automating deployment to Apache Tomcat.
- Understanding the flow of a basic CI/CD pipeline.

## ▶️ Prerequisites

Before reproducing this project, install and configure:

- Git
- Java JDK
- Apache Ant
- Jenkins
- Apache Tomcat
- Required Jenkins plugins and GitHub repository access

**Note:** Configure the JDK, Ant, Jenkins credentials, Tomcat version, and deployment settings according to your environment.

## 📸 Project Demonstration

Add screenshots of the following to this repository to demonstrate your implementation:

- Successful Jenkins FirstJob build
- Successful Checkstyle build
- Successful WAR deployment
  <img width="1905" height="547" alt="Screenshot 2026-10-20 185016" src="https://github.com/user-attachments/assets/2ab9e590-71ae-4c78-89ea-887165616a79" />
  <img width="1902" height="617" alt="Screenshot 2026-10-20 185055" src="https://github.com/user-attachments/assets/a407ef47-b0e0-4bd5-b128-02db105a5e19" />
<img width="1870" height="895" alt="Screenshot 2026-10-20 185117" src="https://github.com/user-attachments/assets/82a06d54-472c-4a93-884c-96740b6b8a56" />

- Running application in the browser
  <img width="1531" height="696" alt="TomcatDeployment" src="https://github.com/user-attachments/assets/9f7e03e4-9ad9-4614-9b3c-a144bedfa33d" />

## 👨‍💻 Author

**Rahimuddin Alam**

- **GitHub:** https://github.com/RahimAlamDevSecOps
- **Portfolio:** https://rahimalamdevsecops.github.io/

---

⭐ If you find this project useful, feel free to explore the repository and share your feedback.

*This is a hands-on learning project built and tested in a local environment.*

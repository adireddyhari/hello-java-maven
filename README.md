## Hello Java Maven – Jenkins CI/CD Build

This project demonstrates how to build a simple Java application using **Maven** in **Jenkins**.  
It is designed as an introductory Continuous Integration (CI) example, running either locally or on a remote server (e.g., AWS EC2).

---

## 📌 Project Overview

This repository contains:
- A basic Java `HelloWorld` application
- A `pom.xml` file for Maven build configuration
- Instructions to set up a Jenkins Freestyle job to build the application

The Jenkins job:
1. Clones this repository from GitHub.
2. Builds the project using Maven (`clean package`).
3. Optionally archives the generated `.jar` file as a build artifact.

---

## 🗂 Project Structure

hello-java-maven/
├── pom.xml
└── src
└── main
└── java
└── HelloWorld.java




- **pom.xml** – Maven build configuration file  
- **HelloWorld.java** – Simple Java class printing a message to the console

---

## 🛠 Prerequisites

Before running this project in Jenkins, ensure you have:

- **Java JDK** (8 or 11 recommended)
- **Maven** (configured in Jenkins)
- **Git** (for cloning this repository)
- **Jenkins** (locally, Docker, or on AWS EC2)
- **Docker** (optional, if running Jenkins in a container)

---

## ⚙️ Setup Instructions

### 1. Clone the Repository
```bash
git clone https://github.com/TechnicalGaur/hello-java-maven.git
cd hello-java-maven
```


## 🚀 Jenkins Setup Guide

# Step 1 – Install Jenkins (Docker Example)

```docker run -d --name jenkins \```
```-p 8080:8080 -p 50000:50000 \```
``` -v jenkins_home:/var/jenkins_home \```
```jenkins/jenkins:lts```


# Step 2 – Configure Maven in Jenkins

Go to Manage Jenkins → Tools → Maven installations

Add Maven (e.g., Maven 3.x) and check Install automatically


# Step 3 – Create a Freestyle Job

New Item → Freestyle project → Name: hello-java-maven

Source Code Management:

  -Select Git

  -Repository URL:
       ```https://github.com/TechnicalGaur/hello-java-maven.git```


  Branch Specifier: */main (or */master if using master branch)

Build → Invoke top-level Maven targets:

Maven Version: Maven 3.x

Goals: clean package

Post-build Actions (Optional):

Archive artifacts: target/*.jar


# Step 4 – Build the Job

Click Build Now

Open the console output to verify BUILD SUCCESS

Download the .jar artifact if archived


## 📄 License

This project is released under the MIT License.


## ✨ Author

Prashant Gour
🔗 GitHub: TechnicalGaur


## Screenshots


<img width="1350" height="582" alt="Screenshot 2025-08-15 140034" src="https://github.com/user-attachments/assets/e5c4c8bc-57a9-477e-9943-5d325b07f776" />



<img width="1337" height="586" alt="Screenshot 2025-08-15 140135" src="https://github.com/user-attachments/assets/4d5d0311-618e-461a-b453-5b0ca8767021" />



<img width="1331" height="555" alt="Screenshot 2025-08-15 140215" src="https://github.com/user-attachments/assets/1c43c887-a8a1-4dbe-a6cb-be137fc71226" />




<img width="1358" height="591" alt="Screenshot 2025-08-15 140253" src="https://github.com/user-attachments/assets/152659a9-9985-4717-a64b-d11c065e9120" />





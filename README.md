# Project-VIII-Continuous-Integration-Using-on-AWS-Cloud


## **Project Overview**
This project focuses on implementing Continuous Integration (CI) using AWS Cloud services to automate the build, test, and notification processes. By leveraging AWS tools, developers can ensure every code commit is tested, reducing errors and improving efficiency.

---

## **Scenario**
- Agile Software Development Life Cycle (SDLC)
- Frequent code changes by developers
- Need for automated build and test processes
- Traditionally managed by Build & Release teams
- Occasional developer involvement in build and test activities

## **Challenges**
- Frequent code changes require consistent testing
- Infrequent testing leads to accumulated bugs and errors
- Developers spend time reworking code due to late error detection
- Manual build and release processes introduce inefficiencies
- Dependencies between teams delay the development cycle
- CI server management incurs operational overhead (Jenkins, Nexus, SonarCloud, etc.)

## **Solution: Continuous Integration on AWS**
- Automate code testing for every commit
- Reduce manual intervention through automated build and test processes
- Notify developers of build and test statuses
- Enable immediate issue resolution and rebuilds
- Utilize cloud services for build, test, and notifications

---

## **Tools & Technologies**
- **Bitbucket** – Code repository
- **AWS CodeArtifact** – Maven dependency management
- **AWS CodeBuild** – Build and test automation
- **SonarCloud** – Code quality and security analysis
- **Amazon S3** – Artifact storage
- **AWS SNS (Simple Notification Service)** – Build and test notifications
- **AWS CodePipeline** – CI/CD pipeline automation

## **Project Objectives**
- Improve fault isolation
- Reduce Mean Time to Repair (MTTR)
- Accelerate feature deployment
- Minimize disruptions to development workflows

---

## **Architecture of Project Services**
- **Version Control:** Bitbucket repository
- **Build & Test:** AWS CodeBuild
- **Code Quality Analysis:** SonarCloud
- **Dependency Management:** AWS CodeArtifact
- **Artifact Storage:** Amazon S3

## **Execution Flow**
### **1. Bitbucket Setup**
- Create an account and repository in Bitbucket
- Establish SSH authentication between the local machine and Bitbucket
- Migrate the VProfile project source code from GitHub to Bitbucket

### **2. AWS CodeArtifact Setup**
- Create a CodeArtifact repository
- Configure `pom.xml` and `settings.xml` for dependency management
- Define build specifications in `buildspec.yml`

### **3. SonarCloud Setup**
- Create a SonarCloud account and set up project details
- Store SonarCloud credentials in AWS Parameter Store
- Reference Parameter Store values in `buildspec.yml`

### **4. AWS CodeBuild Job**
- Understand `buildspec.yml` for build execution
- Update `pom.xml` and `settings.xml` with CodeArtifact repository details
- Create a build job for SonarCloud code analysis

### **5. Execute & Test**
- Execute build jobs for artifact creation
- Validate `buildspec.yml` configurations
- Store build artifacts in an Amazon S3 bucket
- Run AWS CodeBuild to verify successful execution

### **6. AWS CodePipeline Implementation**
- Configure SNS for build and test notifications
- Set up AWS CodePipeline for continuous integration
- Execute and test the end-to-end pipeline

---

## **Conclusion**
By implementing Continuous Integration on AWS, this project streamlines the development workflow, automates testing, and reduces operational overhead. The use of cloud-native services ensures scalability, efficiency, and rapid feedback for developers, leading to improved software quality and faster feature releases.


Author 👨🏽‍💻: Dany Christel 

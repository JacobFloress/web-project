# CI/CD Pipeline on AWS

This project is an **end-to-end Continuous Integration and Continuous Deployment (CI/CD) pipeline** built on **Amazon Web Services (AWS)**. It automates the full software delivery lifecycle—from code commits to build, testing, packaging, and deployment—using modern DevOps practices.

---

## Project Overview
- Automated **build, test, and deploy workflows** triggered on each GitHub commit.  
- Implemented **infrastructure as code** with AWS CloudFormation for repeatable and scalable environments.  
- Integrated multiple AWS services for a production-style pipeline:
  - **AWS CodeArtifact** → Secure package & dependency management  
  - **AWS CodeBuild** → Continuous integration (build & test automation)  
  - **AWS CodeDeploy** → Automated deployments to EC2 instances  
  - **AWS CodePipeline** → Orchestration of the end-to-end pipeline  
  - **Amazon S3** → Artifact storage  

---

## Key Features
- **Web Application Deployment**: Hosted a Java web app on AWS EC2 with Apache Tomcat & Apache HTTP server.  
- **Secure Remote Development**: Configured remote SSH access via VS Code for direct cloud development.  
- **Automated Builds**: Used `buildspec.yml` to define build phases (install, pre-build, build, post-build).  
- **Deployment Automation**: Managed lifecycle events with `appspec.yml` and shell scripts (`install_dependencies.sh`, `start_server.sh`, `stop_server.sh`).  
- **End-to-End Pipeline**: A single GitHub commit triggers build, artifact packaging, and deployment to a live environment.

---

## 📝 Lessons Learned
- Gained hands-on experience with **IAM roles, permissions, and security best practices**.  
- Learned to **troubleshoot build & deployment errors** using AWS CloudWatch logs.  
- Built a **portfolio-ready DevOps project** showcasing automation at scale.  

---

## ⚙️ Tech Stack
- **AWS Services**: EC2, CodePipeline, CodeBuild, CodeDeploy, CodeArtifact, CloudFormation, S3  
- **Languages & Tools**: Java, Maven, Bash, Git, GitHub, VS Code  

---

## ▶️ How It Works
1. Developer pushes code to GitHub  
2. CodePipeline triggers and fetches the source  
3. CodeBuild compiles, tests, and packages the app into an artifact (WAR file)  
4. Artifact is uploaded to S3  
5. CodeDeploy retrieves the artifact, runs lifecycle scripts, and deploys the app to EC2  
6. Application is updated live 🎉  

---

## 📂 Repository Structure
- buildspec.yml # Build instructions for CodeBuild
- appspec.yml # Deployment instructions for CodeDeploy
- scripts/ # Lifecycle event scripts (install/start/stop)
- src/ # Java application source code

---

## 🌐 Live Demo
Provisioned and deployed on AWS EC2; decommissioned resources after testing to avoid charges

---

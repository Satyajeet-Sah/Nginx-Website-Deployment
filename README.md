# Nginx Website Deployment with GitHub Actions CI/CD

A hands-on DevOps project demonstrating automated deployment of a static website to an AWS EC2 Ubuntu instance using Nginx and GitHub Actions. Every code push to the `main` branch automatically deploys the latest website changes to the EC2 server through an SSH-based CI/CD pipeline.

---

## 🚀 Project Overview

This project demonstrates how to automate website deployment using GitHub Actions.

Instead of manually copying website files to the server after every update, the deployment process is fully automated. Whenever changes are pushed to the GitHub repository, GitHub Actions securely connects to the EC2 instance via SSH and updates the website automatically.

---

## ✨ Key Features

- Deploy a static website using Nginx
- Host the website on AWS EC2 (Ubuntu)
- Automated deployment with GitHub Actions
- SSH-based secure deployment
- Version-controlled website source code
- Automatic website updates on every push to the `main` branch

---

## 🛠 Technologies Used

- AWS EC2
- Ubuntu Server
- Nginx
- Git
- GitHub
- GitHub Actions
- YAML
- SSH

---

## 🏗 Architecture

```
Developer
     │
     │ git push
     ▼
GitHub Repository
     │
     ▼
GitHub Actions Workflow
     │
SSH Connection
     ▼
AWS EC2 (Ubuntu)
     │
Git Pull
     ▼
Nginx Web Server
     │
     ▼
Website Updated Automatically
```

---

## ☁ AWS Services Used

- Amazon EC2
- Security Groups

---

## ⚙ EC2 Configuration

- Ubuntu Server 24.04/26.04 LTS
- Instance Type: t3.micro
- SSH access using Key Pair
- Security Group Configuration:
  - SSH (22)
  - HTTP (80)

---

## 🔄 CI/CD Workflow

The deployment pipeline is triggered automatically whenever code is pushed to the `main` branch.

### Workflow Steps

1. Push code to GitHub
2. GitHub Actions starts automatically
3. Repository is checked out
4. SSH connection is established with the EC2 instance
5. Navigate to the Nginx web directory
6. Pull the latest changes from GitHub
7. Website is updated instantly

---

## 📁 Repository Structure

```
.
├── .github/
│   └── workflows/
│       └── deploy.yml
├── index.html
└── README.md
```

---

## 🔐 GitHub Secrets Used

The workflow securely authenticates using GitHub Secrets.

| Secret | Purpose |
|---------|---------|
| EC2_HOST | EC2 Public IP |
| EC2_USER | SSH Username |
| EC2_SSH_KEY | Private SSH Key |

---

## 📄 Deployment Workflow

The GitHub Actions workflow performs the following deployment:

- Trigger on push to `main`
- Checkout repository
- Connect to EC2 using SSH
- Pull latest code
- Deploy updated website automatically

---

## 📸 Screenshots

- AWS EC2 Instance
- GitHub Actions Workflow
- Successful Deployment Logs
- Nginx Running
- Live Website

---

## 🎯 Learning Outcomes

Through this project, I learned how to:

- Deploy websites on AWS EC2
- Configure and manage Nginx
- Create GitHub Actions workflows
- Automate deployments using CI/CD
- Securely connect to remote servers using SSH
- Use GitHub Secrets for secure authentication
- Implement infrastructure automation for web deployment

---

## 👨‍💻 Author

**Satyajeet**

DevOps | AWS | Linux | GitHub Actions | Automation

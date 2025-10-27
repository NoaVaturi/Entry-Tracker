# 🧾 EntryTracker – CI/CD DevOps Project

A complete **CI/CD pipeline** for a Python/Flask web application, demonstrating real-world DevOps automation — from **testing and containerization** to **cloud deployment on AWS EC2** via **GitHub Actions**.

---

## 🏗️ Project Overview
EntryTracker is a lightweight Flask-based web application that allows users to manage and track personal or system entries stored in **MongoDB**.
The goal of this project is to showcase a **fully automated DevOps pipeline** that builds, tests, packages, and deploys the app to the cloud — all triggered directly from GitHub.

---

## 🧰 Tech Stack

| Category | Technologies |
|-----------|---------------|
| **Backend** | Flask · Python · MySQL |
| **CI/CD** | GitHub Actions |
| **Containerization** | Docker · Docker Compose |
| **Cloud Infrastructure** | AWS EC2 · AWS ECR |
| **Testings** | Pytest |

---

## 📊 Architecture Diagram
<img width="1141" height="315" alt="diagram-v1" src="https://github.com/user-attachments/assets/ee0818c0-cc63-4733-9c32-1151f1386726" />


---

## 🚀 Workflow Summary

| Stage | Description |
|-------|--------------|
| 🧑‍💻 **Commit** | Developer pushes code to GitHub |
| 🧪 **Test** | Unit tests executed via Pytest |
| 🐳 **Build & Push** | Image uploaded to AWS ECR |
| ☁️ **Deploy** | GitHub Actions connects to EC2 instance via SSH |
| 🔁 **Compose Up** | EC2 pulls the latest image and restarts the Docker Compose stack |

---

## 🗂️ Project Structure

```
.
├── .github/
│   └── workflows/
│       └── application.yml             # GitHub Actions pipeline (test, build, push, deploy)
│
├── app.py                        # Flask application entry point
├── docker-compose.yml            # Docker Compose for EC2 deployment
├── Dockerfile                    # Image build configuration
├── nginx.conf                    # Nginx reverse proxy configuration
├── wait-for-flask.sh             # Helper script to ensure Flask is ready before tests
├── requirements.txt              # Python dependencies
├── .env                          # Environment variables (not committed in production)
```

---

## 📁 Repository Breakdown
| Repository | Description | Visibility |
|-------------|-------------|------------|
| 🔹 **[entryTracker_cicd](https://github.com/NoaVaturi/entryTracker_cicd.git)** | Flask-based web application integrated with a complete CI/CD pipeline using GitHub Actions. Automates testing, Docker image builds, ECR uploads, and EC2 deployments via SSH. | 🔒 Private |

🧭 *Code is private due to sensitive credentials but available for review upon request.*


---

## ⚙️ Key Features
| Feature | Description |
|----------|--------------|
| ✅ CI/CD Automation | Full pipeline from commit → test → ECR push → EC2 deploy |
| ✅ Secure Deployments | SSH integration with GitHub Secrets |
| ✅ Centralized Image Management | AWS ECR used for storing and versioning Docker images |
| ✅ Production-ready Compose | Docker Compose handles environment startup and restarts |

---

## 🧠 Challenges & Learnings
| Challenge | Solution |
|------------|-----------|
| Automating remote EC2 deployments | Integrated SSH-based deployment via GitHub Actions |
| Managing secrets securely | Stored AWS & SSH credentials in GitHub Secrets |
| ECR authentication issues | Solved using aws-actions/amazon-ecr-login |
| Deployment downtime | Used docker-compose down && docker-compose up -d for smooth restarts |

---

## 📚 Related Template Repos
*(Coming soon – sanitized public versions of each module for learning use.)*

---

## 🧩 Tools Used
`AWS` · `Docker` · `MySQL` · `Pytest` · `GitHub Actions` · `Python` · `Docker Compose`

---

## 👩‍💻 Author
**Noa Vaturi**  
💼 [LinkedIn](https://linkedin.com/in/noavaturi) · 💻 [GitHub](https://github.com/NoaVaturi)

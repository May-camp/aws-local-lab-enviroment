# 🚀 AWS LocalStack Lab Environment

This repository documents my process for setting up a full AWS-compatible cloud environment on a local **Ubuntu** machine. This allows for rapid testing of Cloud/DevOps workflows without incurring AWS costs.

## 🛠 System Architecture
The setup utilizes **Docker** to containerize AWS services, allowing for a clean and reproducible development environment. 

## ⚙️ Installation & Configuration
I used a combination of the LocalStack CLI and `awslocal` for a seamless workflow.

### 1. Docker Configuration
I ensured the Docker daemon was running and my user had the necessary permissions to manage containers:
```bash
sudo systemctl start docker
sudo usermod -aG docker $USER

# 🚀 AWS LocalStack Lab Environment

This repository documents my process for setting up a full AWS-compatible cloud environment on a local **Ubuntu** machine. This allows for rapid testing of Cloud/DevOps workflows without incurring AWS costs.

## 🛠 System Architecture
The setup utilizes **Docker** to containerize AWS services, allowing for a clean and reproducible development environment. 

# Update package list
sudo apt-get update

# Install Docker
sudo apt-get install docker.io -y

# Start and enable Docker service
sudo systemctl start docker
sudo systemctl enable docker

# Crucial: Add your user to the docker group to run commands without 'sudo'
sudo usermod -aG docker $USER

# Ensure Python and Pip are installed
sudo apt install python3-pip -y

# Install LocalStack CLI
pip install localstack  --break-system-packages

# Verify the installation
localstack --version

# Start LocalStack in detached mode (background)
localstack start -d

# Check the status of the services
localstack status services

## ⚙️ Installation & Configuration
I used a combination of the LocalStack CLI and `awslocal` for a seamless workflow.

### 1. Docker Configuration
I ensured the Docker daemon was running and my user had the necessary permissions to manage containers:
```bash
sudo systemctl start docker
sudo usermod -aG docker $USER

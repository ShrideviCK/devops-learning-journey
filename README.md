             DevOps Learning Journey 🚀
About Me

I am a DevOps Professional with 11 years of IT experience. After returning from maternity leave and a career break, I started rebuilding my hands-on DevOps skills from scratch.

This repository documents my learning journey, labs, projects, notes, and hands-on practice covering Linux, Git, Docker, Kubernetes, Terraform, Jenkins, AWS, and DevOps automation.

Environment Setup
Laptop Configuration
HP Laptop
Windows 11
WSL2 (Ubuntu)
Docker Desktop
VS Code
Git
GitHub
Jenkins (Docker Container)
Initial Setup Activities
Step 1: Windows Setup
Updated Windows
Installed latest updates
Installed developer tools
Step 2: WSL Installation

Installed Ubuntu using WSL2.

PowerShell
wsl --install

Verified installation:

PowerShell
wsl -l -v
Step 3: Ubuntu Configuration

Updated packages:

Shell
sudo apt update
sudo apt upgrade -y

Installed utilities:

Shell
sudo apt install curl wget unzip vim jq tree htop -y
Step 4: Git Setup

Installed Git in Ubuntu.

Verified version:

Shell
git --version

Configured Git:

Shell
git config --global user.name "Shridevi"
git config --global user.email "your-email@example.com"

Verified:

Shell
git config --global --list
Step 5: Docker Setup

Installed Docker Desktop.

Enabled:

WSL Integration
Ubuntu Integration

Verified:

Shell
docker --version

Tested:

Shell
docker run hello-world
Step 6: Jenkins Setup

Started Jenkins using Docker.

Shell
docker run -d \
--name jenkins \
-p 8080:8080 \
-p 50000:50000 \
jenkins/jenkins:lts
 

Verified:

Shell
docker ps
 

Accessed Jenkins:

Plain Text
http://localhost:8080

Retrieved administrator password:

Shell
docker exec -it jenkins cat /var/jenkins_home/secrets/initialAdminPassword

Installed suggested plugins.

Created administrator account.

Step 7: GitHub Repository Setup

Created repository:

Plain Text
devops-learning-journey

Initialized repository:

Shell
git init

Added remote repository.

Verified:

Shell
git remote -v
Step 8: SSH Authentication Setup

Generated SSH Key:

Shell
ssh-keygen -t ed25519 -C "email@example.com"

Started SSH Agent:

Shell
eval "$(ssh-agent -s)"

Added key:

Shell
ssh-add ~/.ssh/id_ed25519

Added public key to GitHub.

Updated repository remote:

Shell
git remote set-url origin git@github.com:ShrideviCK/devops-learning-journey.git

Verified:

Shell
ssh -T git@github.com

Successfully configured passwordless GitHub authentication.

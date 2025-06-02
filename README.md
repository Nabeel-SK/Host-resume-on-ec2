# Host Your Resume on AWS EC2 with a CI/CD Setup Using GitHub Actions

This project automatically deploys the latest version of my HTML resume to an AWS EC2 instance using GitHub Actions.

### 🔧 How it works:
- On every push to the `main` branch:
  1. The HTML code is securely copied to the EC2 server via SSH.
  2. Apache is installed and started (if not already).
  3. The resume files are moved to `/var/www/html` to serve them publicly.

### 🛠️ Tech Stack:
- GitHub Actions
- Ubuntu EC2 Instance
- Apache Web Server
- SSH Deployment

### 🔐 Secrets Required:
- `EC2_SSH_KEY` – Your PEM private key
- `HOST_DNS` – EC2 public DNS
- `USERNAME` – EC2 user (usually `ubuntu`)
- `TARGET_DIR` – Path on EC2 (e.g., `/home/ubuntu/resume`)

---


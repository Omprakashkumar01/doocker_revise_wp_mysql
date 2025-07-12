# 🐳 WordPress + MySQL Deployment using Docker Compose on RHEL

This project sets up a **WordPress site** with a **MySQL database** using Docker Compose on a **Red Hat Enterprise Linux (RHEL)** environment. It simplifies the manual setup into a clean and maintainable YAML configuration.

<img width="1200" height="1200" alt="My personalized network (mynet)" src="https://github.com/user-attachments/assets/de0312d8-3d83-424e-88a3-50d0dd29b030" />
---

## 📦 Project Structure

```
.
├── docker-compose.yml
└── README.md
```
## 🚀 Getting Started
✅ Prerequisites
* RHEL (Red Hat Enterprise Linux)

*Docker and Docker Compose v2

## 🔧 Install Docker and Compose (If Not Installed)
```
sudo yum install -y yum-utils
sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
sudo yum install -y docker-ce docker-ce-cli containerd.io
sudo systemctl start docker
sudo systemctl enable docker
```

# Install Docker Compose plugin
```
mkdir -p ~/.docker/cli-plugins/
curl -SL https://github.com/docker/compose/releases/latest/download/docker-compose-linux-x86_64 \
  -o ~/.docker/cli-plugins/docker-compose
chmod +x ~/.docker/cli-plugins/docker-compose
```
# Verify installation
```
docker compose version
```

## 📂 Volumes
/data:/var/www/html/ – stores WordPress content.

/db:/var/lib/ – stores MySQL database files.

## 🧠 Environment Variables

Variable	Description

MYSQL_USER	MySQL user for WordPress
MYSQL_PASSWORD	Password for the above user
MYSQL_ROOT_PASSWORD	Root password for MySQL

🚀 How to Run
```
docker compose up -d
```
🌐 Access the Application
Visit:
👉 http://localhost:8080 (or your server’s IP)
to complete the WordPress installation setup.


<img width="1272" height="795" alt="Screenshot 2025-07-12 233905" src="https://github.com/user-attachments/assets/7be095c5-f0a5-4630-b3e7-1041b94743e8" />


# Redash Self-hosted Installation Guide (Docker-based)

This guide walks you through setting up a machine to host Redash using Docker and Docker Compose.

---

## 🖥️ Machine Requirements

| Component         | Minimum                    
|------------------|----------------------------|
| **CPU**          | 2 cores                    |
| **Memory (RAM)** | 4 GB                       |
| **Disk**         | 20 GB SSD                  | 
| **OS**           | Ubuntu 20.04 / 22.04 LTS   |
| **Network**      | Internet access required   | 

---

## ⚙️ Step-by-Step Installation

### 1. Update System

```bash
sudo apt update && sudo apt upgrade -y
```

### 2. Install Docker and Docker Compose

```bash
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh
sudo apt install docker-compose -y
```

Optional (to run docker without sudo):

```bash
sudo usermod -aG docker $USER
newgrp docker
```

### 3. Install `pwgen`

```bash
sudo apt install pwgen -y
```

### 4. Clone Redash Setup Repo

```bash
git clone https://github.com/getredash/setup.git
cd setup
```

### 5. Run Setup Script

```bash
sudo ./setup.sh
```

This sets up Docker containers for Redash, PostgreSQL, and Redis.

---

## 🌐 Access Redash

Visit `http://<your-server-ip>` in your browser.


## 🧾 Credits

Based on the official Redash Docker setup: https://github.com/getredash/setup

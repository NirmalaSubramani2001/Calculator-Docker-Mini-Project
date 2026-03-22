# Calculator-Docker-Mini-Project

# 🧮 Docker Calculator App

A simple web-based calculator application containerized using Docker. This project demonstrates basic containerization and deployment using Docker.

---

## 🚀 Features
- Simple and responsive calculator UI
- Lightweight HTML-based application
- Containerized using Docker
- Easy to run on any system

---

## 🛠️ Tech Stack
- HTML
- Docker
- Node.js (for serving static files)

---

## 📁 Project Structure
Docker-Mini-Project/
│── Dockerfile
│── calculator.html
│── README.md

---

## 🐳 Docker Setup

### 🔹 Build Docker Image
```bash
docker build -t calculator .

🔹 Run Container
docker run -d -p 5000:5000 --name calculator-app calculator

🌐 Access Application

Open your browser:
http://localhost:5000


💡 Learning Outcomes
Learned Docker basics (build, run, containerization)
Understood Dockerfile creation
Hands-on experience with real project deployment

## 🔹 Step 1: To Run the app
```bash
docker run -d -p 5000:5000 calculator

OUTPUT :

<img width="1217" height="946" alt="image" src="https://github.com/user-attachments/assets/80b2a99f-77f2-4c7c-8cfb-ad3474afe324" />
https://1drv.ms/i/c/351c3fb795fe3dba/IQBQqoYC5_uJRr3t1ugX5AUfAU0f3iLnVdzXIeE50cSZeRI?e=d1J9r5


✅ Step-by-Step Fix (WSL + Docker Desktop)

🔹 Step 1: Check Docker Desktop is running (Windows)

Open Windows and start:
👉 Docker Desktop

Wait until it shows:

Docker is running


🔹 Step 2: Enable WSL integration

In Docker Desktop:

⚙️ Settings → Resources → WSL Integration

✔ Enable:

Your Ubuntu distro (example: Ubuntu-22.04)

Click:
👉 Apply & Restart


🔹 Step 3: Restart WSL

In PowerShell (Windows):

wsl --shutdown

Then reopen your Ubuntu terminal


🔹 Step 4: Test Docker

In WSL terminal:

docker version

If working → you’ll see client & server info ✅

🔴 If STILL getting permission denied

Run inside WSL:

sudo usermod -aG docker $USER
newgrp docker


🔹 Step 5: Fix Docker socket (WSL specific)

Sometimes WSL needs this:

sudo chmod 666 /var/run/docker.sock

⚠️ This is temporary but useful for testing


🔹 Step 6: Try your build again

docker build -t calculator .

🟡 Fix BuildKit warning (optional)

echo 'export DOCKER_BUILDKIT=1' >> ~/.bashrc
source ~/.bashrc



Since you're learning, don’t get stuck here. Just disable BuildKit and continue:

export DOCKER_BUILDKIT=0

Then run:

docker build -t calculator .

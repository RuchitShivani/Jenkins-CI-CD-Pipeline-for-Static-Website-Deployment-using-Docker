# 🚀 Jenkins CI/CD Pipeline for Static Website Deployment using Docker (No Git Integration)

This project demonstrates how to build a simple CI/CD pipeline using **Jenkins** and **Docker** to automate the deployment of a static HTML website — all **without using Git or GitHub**.

## 🎯 Goal

Automate the build and deployment process of a basic static website using:
- Jenkins for CI/CD
- Docker for containerization
- NGINX to serve HTML
- Local files instead of a Git repository

---

## ✅ Steps Followed

### 1. 🧱 Frontend Setup
- Created a simple `index.html` file.
- Built a `Dockerfile` using `nginx:alpine` to serve the HTML content.

### 2. 🔁 Jenkins Pipeline Configuration
- **Step 1: Copy HTML files**  
  Manually copied local project files into a Jenkins workspace or designated folder.
  
- **Step 2: Docker Build**  
  Jenkins executes the Docker build command using the Dockerfile.

- **Step 3: Docker Run**  
  The newly built Docker image is run on a local port:
  - Initially tried on `8088`
  - Switched to `8090` due to port conflicts

### 3. 🛠️ Issues & Fixes
- **Dockerfile not found error**  
  → Resolved by navigating Jenkins to the correct working directory.
  
- **Port already in use**  
  → Resolved by changing the port to one that was not in use (`8090`).

---

## 🚢 Result

- Website successfully deployed inside a Docker container.
- Accessible locally at:  
  [http://localhost:8089]
![Screenshot 2025-04-17 184852](https://github.com/user-attachments/assets/405988b5-32f2-4e3d-954f-eb7bd998bf20)
![Screenshot 2025-04-17 185200](https://github.com/user-attachments/assets/896c1d4d-606a-4283-8dcb-0cb715c34ff0)

---


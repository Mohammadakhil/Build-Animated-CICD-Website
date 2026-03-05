# CI/CD Pipeline Blueprint 🚀
**Date:** 05-Mar-2026  
**Developer:** Mohammad Akhil

---

## 📝 Overview
A modern, automated deployment pipeline demonstrating containerization and continuous delivery. This project takes a simple web application and automates the build and distribution process using industry-standard DevOps tools.

---

## 🛠 Tech Stack
* **Docker:** Used for consistent containerization of the web environment, ensuring the application runs identically in every environment.
* **GitHub Actions:** The automation engine used to trigger the build and push workflow upon every code change.
* **GHCR (GitHub Container Registry):** Serves as the high-performance, secure cloud hosting service for Docker images.
* **Automation:** Implements end-to-end delivery logic, transforming a simple code push into a live, available container image.

---

## 🏗 Architecture
The pipeline follows a five-stage lifecycle:
1.  **Develop:** The HTML content and the Dockerfile configuration are authored and tested locally.
2.  **Push:** Code is committed and pushed to the `main` branch of the GitHub repository.
3.  **Automate:** A GitHub Actions runner triggers automatically, builds the new Docker image, and authenticates with GHCR.
4.  **Registry:** The finalized image is securely stored within the GitHub Container Registry.
5.  **Deploy:** The application is "decoupled" from the source code and can be pulled and run on any server with a single command.

---

## 🚀 Getting Started

### Prerequisites
* **Docker** installed locally to build or run the container.

### Running the App (The Modern Way)
You don't even need to clone this repository to run the app. You can pull the pre-built image directly from the cloud using this command:


docker run -d -p 9000:80 ghcr.io/mohammadakhil/build-animated-cicd-website:main

💻 Local Development & Build
If you wish to build and modify the image manually on your local machine, follow these steps:

1. Clone the repository First, download the source code to your local environment:

git clone https://github.com/Mohammadakhil/Build-Animated-CICD-Website.git
2. Build the image locally Use Docker to package the application into an image:

docker build -t my-app .
3. Run the local container Start the application and map it to your local port 8080:

docker run -p 8080:80 my-app

**Created by Mahammad Akhil as a DevOps Portfolio Project.**

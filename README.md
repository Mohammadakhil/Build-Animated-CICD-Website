Day 05-mar-26
CI/CD Pipeline Blueprint 🚀
A modern, automated deployment pipeline demonstrating containerization and continuous delivery. This project takes a simple web application and automates the build and distribution process using industry-standard DevOps tools.

🛠 Tech Stack
Docker: For consistent containerization of the web environment.

GitHub Actions: To automate the build and push workflow.

GHCR (GitHub Container Registry): For secure cloud hosting of Docker images.

Automation: End-to-end delivery from code push to image availability.

🏗 Architecture
Develop: HTML and Dockerfile are created locally.

Push: Code is pushed to the main branch.

Automate: GitHub Actions triggers on the push, builds the Docker image, and authenticates with GHCR.

Registry: The final image is stored in GitHub Container Registry.

Deploy: The application can be pulled and run on any server with a single command.

🚀 Getting Started
Prerequisites
Docker installed locally.

Running the App (The Modern Way)
You don't even need to clone this repository to run the app. You can pull the pre-built image directly from the cloud:

Bash
docker run -d -p 9000:80 ghcr.io/mohammadakhil/build-animated-cicd-website:main
Navigate to http://localhost:9000 to view the live site.

Local Development & Build
If you wish to build the image manually:

Clone the repo:

Bash
git clonehttps://github.com/Mohammadakhil/Build-Animated-CICD-Website.git
Build the image:

Bash
docker build -t my-app .
Run locally:

Bash
docker run -p 8080:80 my-app
🤖 CI/CD Workflow
The automation logic is defined in .github/workflows/publish.yml.

Authentication: Uses GITHUB_TOKEN for secure login.

Efficiency: Uses nginx:alpine as a base image to keep the footprint under 10MB.

Tagging: Automatically tags images with latest and the unique Git commit SHA.

Created by Mahammad Akhil as a DevOps Portfolio Project.

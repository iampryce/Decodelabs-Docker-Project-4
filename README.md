# Decodelabs Docker Project 4

![Docker](https://img.shields.io/badge/Docker-Containerized-blue)
![Nginx](https://img.shields.io/badge/Nginx-Alpine-green)

A DevOps project focused on containerizing a static HTML application using Docker and Nginx.

---

# Project Objective

* Understand containerization concepts
* Build a Docker image
* Run containers locally
* Learn Docker workflow and deployment basics

---

# Project Architecture

```text
Application Code
      ↓
Dockerfile
      ↓
Docker Image
      ↓
Running Container
      ↓
Accessible Web Application
```

---

# Technologies Used

* Docker
* Dockerfile
* Nginx (Alpine)
* HTML

---

# Repository Structure

```bash
Decodelabs-Docker-Project-4/
│
├── app/
│   └── index.html
│
├── Dockerfile
├── docker-compose.yml
└── README.md
```

---

# Dockerfile

```dockerfile
FROM nginx:alpine

COPY app/ /usr/share/nginx/html/

EXPOSE 80
```

---

# Build the Docker Image

```bash
docker build -t decodelabs-project4:latest .
```

---

# Run the Container

```bash
docker run -d -p 80:80 --name decodelabs-project4 decodelabs-project4:latest
```

---

# Verify Running Containers

```bash
docker ps
```

---

# Open in Browser

```text
http://localhost:80
```

---

# Run with Docker Compose

```bash
docker compose up -d
```

Stop the container:

```bash
docker compose down
```

---

# Useful Docker Commands

```bash
docker ps
docker logs decodelabs-project4
docker stop decodelabs-project4
docker rm decodelabs-project4
docker rmi decodelabs-project4:latest
```

---

# Key Learning Outcomes

* Writing Dockerfiles
* Building Docker images
* Running containers
* Port mapping
* Detached mode containers
* Basic containerization workflow

---

# Author

Oluwatobi Ogundimu

Developed as part of the DecodeLabs DevOps Industrial Training Program 2026.

---

# License

MIT License

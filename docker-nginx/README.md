# Docker Nginx Website

## Project Overview
This is my first Docker project as part of my DevOps learning journey. It uses Nginx to serve a custom HTML webpage from a Docker container.

## Project Structure

- `Dockerfile`: Defines how the Docker image is built.
- `index.html`: Contains the custom website displayed by Nginx.
- `README.md`: Project documentation.

## Technologies Used
- Docker
- Nginx
- HTML

## Build the Docker Image

```bash
docker build -t devops-nginx:v1 .
```

## Run the Container

```bash
docker run -d --name my-nginx -p 8081:80 devops-nginx:v1
```

Open the website in your browser:

`http://localhost:8081`

## Troubleshooting

During this project, I intentionally used an incorrect port mapping:

```bash
docker run -d --name my-nginx -p 8081:81 devops-nginx:v1
```

The website was inaccessible because Nginx listens on port 80 inside the container, not port 81.

### Commands Used to Diagnose the Issue

```bash
docker ps
docker logs my-nginx
```

The `docker ps` output showed that host port 8081 was mapped to container port 81.

### Solution

I corrected the port mapping:

```bash
docker run -d --name my-nginx -p 8081:80 devops-nginx:v1
```

The website then became accessible.

## What I Learned

- How to create a Dockerfile.
- How to build and run a Docker image.
- How Docker port mapping works.
- How to inspect containers and read logs.
- How to troubleshoot a container networking issue.

---

**Part of my DevOps Journey – 2026**s
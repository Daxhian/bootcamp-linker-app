# Docker Setup for Next.js Fullstack Application

This document describes how I containerized a full-stack Next.js application consisting of a Next.js frontend and a NestJS backend (with PostgreSQL database) using multi-stage Dockerfiles and Docker Compose for local testing.

### Frontend application repo: 
```
https://github.com/Daxhian/devops-bootcamp-frontend
```

### Backend application repo: 
```
https://github.com/Daxhian/devops-bootcamp-backend
```

### Goals
- Build lightweight, production-ready docker images
- Demonstrate containerization skills for deployment


## How I Built & Tested Locally
 Since the Docker images are stored in my public Docker Hub repository, the instructions in the Docker Compose file simply pull the images and start the containers. 

- A database is required for the backend application to run, so I included a PostgreSQL database container in the Docker Compose file.
![Alt text](/images/docker_repository.png)

### Steps to run the Conatiner using Docker compose
1. Start the application stack (containers)
```
docker compose up -d
```

2. View logs
```
docker compose logs -f
```
![Alt text](/images/app_running_docker_logs.png)

3. Stop the stack temporarily 
```
docker compose stop
```

4. Restart after stopping
```
docker compose start
```

4. Stop and Clean up
```
docker compose down
```


### Test the application locally
```
http://localhost:3000
```
![Alt text](/images/app_running_on_browser.png)
# Assignment 2 (Docker and Dockerhub) Answers:
---
<img src="https://user-images.githubusercontent.com/43959475/193852439-ecf91e2d-c234-40d6-9639-10302efd9ab5.gif" width="30%" height="30%"/>

---
## Task 1: ( 15 basic Docker commands )


### docker version :
```bash
docker version
```

### docker images :
```bash
docker images
```

### docker build :
```bash
docker build -t sammg/welcome-app
```

### docker start :
```bash
docker stop 859d3d738ade
docker ps -a
```

### docker stop :
```bash
docker stop 859d3d738ade
docker ps -a
```

### docker run :
```bash
docker run -d -p 8080:5051 sammg/welcome-app
docker ps -a
```

### docker ps :
```bash
docker ps -a
```

### docker inspect :
```bash
docker inspect 9b0c19e9f73c
```

### docker logs :
```bash
docker logs 9b0c19e9f73c
```

### docker diff :
```bash
docker diff 9b0c19e9f73c
```

### docker save :
```bash
docker save sammg/welcome-app > welcome-app.tar
```

### docker load :
```bash
docker load < welcome-app.tar
```

### docker exec :
```bash
docker exec -it 9b0c19e9f73c bash
```

### docker rename :
```bash
docker ps -a
docker rename boring_bohr welcome_container
docker ps -a
```

### docker rm :
```bash
docker rm -f 2ae2b8e80563
```

### docker rmi :
```bash
docker rmi sammg/welcome-app
```

---

# Task 2:

### Running [Hello World Docker Image](https://hub.docker.com/_/hello-world):

### Task Screenshots:
```bash
docker pull hello-world
docker run hello-world
```

---

# Task 3:

### Hello world fastapi application Screenshots:
```bash
docker build -t sammg/fastapi-hello .
docker run -d -p 5055:8000 sammg/fastapi-hello
docker ps -a
docker logindocker
```

###  Dockerfile for your fastapi hello world application Screenshots:

### Run and Push docker image to DockerHub Screenshots:

#### Dockerhub Link for image:
https://hub.docker.com/r/sammg/fastapi-hello

---

# Task 4:

### : GH Actions for build and deploy to Dockerhub:

### Repo link:

https://github.com/Samm-G/fastapi-dockerhub-deploy

### Github Actions run and published:


### Dockerhub Image:

https://hub.docker.com/r/sammg/fastapi-hello-auto

---
---

---
---

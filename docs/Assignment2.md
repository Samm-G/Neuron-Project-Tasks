# Assignment 2 (Docker and Dockerhub) Answers:
---
<img src="https://user-images.githubusercontent.com/43959475/193852439-ecf91e2d-c234-40d6-9639-10302efd9ab5.gif" width="30%" height="30%"/>

---
## Task 1: ( 15 basic Docker commands )


### docker version :
```bash
docker version
```
![docker-version](https://user-images.githubusercontent.com/43959475/196885503-d317d9ba-a480-49d0-b485-af18494d81d2.jpg)

### docker images :
```bash
docker images
```
![docker-images](https://user-images.githubusercontent.com/43959475/196885529-90065eae-80cb-4985-89b7-f71679ae3a63.jpg)

### docker build :
```bash
docker build -t sammg/welcome-app
```
![docker-build-1](https://user-images.githubusercontent.com/43959475/196885563-e800ac91-1b57-4944-9506-4cb696c2e18d.jpg)
![docker-build-2](https://user-images.githubusercontent.com/43959475/196885576-8355af1f-b01f-450f-97bd-2a23a9ccb841.jpg)

### docker start :
```bash
docker stop 859d3d738ade
docker ps -a
```
![docker-start](https://user-images.githubusercontent.com/43959475/196885611-e69bc3aa-1229-4be3-97de-9cd54f34c011.jpg)

### docker stop :
```bash
docker stop 859d3d738ade
docker ps -a
```
![docker-stop](https://user-images.githubusercontent.com/43959475/196885636-65db618a-32aa-4342-84e8-ec8ca6cd81d0.jpg)

### docker run :
```bash
docker run -d -p 8080:5051 sammg/welcome-app
docker ps -a
```
![docker-run](https://user-images.githubusercontent.com/43959475/196885662-2ef5ea92-7d8d-41f3-8339-6681a78f92aa.jpg)

### docker ps :
```bash
docker ps -a
```
![docker-ps](https://user-images.githubusercontent.com/43959475/196885680-990a148e-8fe1-469f-ae96-c34f131fa431.jpg)

### docker inspect :
```bash
docker inspect 9b0c19e9f73c
```
![docker-inspect](https://user-images.githubusercontent.com/43959475/196885699-d7efdd00-6dae-4dac-9f26-5559cd34e614.jpg)

### docker logs :
```bash
docker logs 9b0c19e9f73c
```
![docker-logs](https://user-images.githubusercontent.com/43959475/196885709-df3497c8-b5dc-4b59-bbdf-bd4bc807c85a.jpg)

### docker diff :
```bash
docker diff 9b0c19e9f73c
```
![docker-diff](https://user-images.githubusercontent.com/43959475/196885721-a35b7fa6-d74d-487a-af75-5b1888d6cf47.jpg)

### docker save :
```bash
docker save sammg/welcome-app > welcome-app.tar
```
![docker-save](https://user-images.githubusercontent.com/43959475/196885751-605ad278-9a72-454b-b0ad-c8cca3265832.jpg)

### docker load :
```bash
docker load < welcome-app.tar
```
![docker-load](https://user-images.githubusercontent.com/43959475/196885772-6da64523-24f9-4683-a71c-a0b26bcfebd6.jpg)

### docker exec :
```bash
docker exec -it 9b0c19e9f73c bash
```
![docker-exec](https://user-images.githubusercontent.com/43959475/196885798-b7685fc7-4018-4ef9-8a9b-ec54668ee7d4.jpg)

### docker rename :
```bash
docker ps -a
docker rename boring_bohr welcome_container
docker ps -a
```
![docker-rename](https://user-images.githubusercontent.com/43959475/196885816-bc84b711-0013-4088-8adb-cec28188cfb2.jpg)

### docker rm :
```bash
docker rm -f 2ae2b8e80563
```
![docker-rm](https://user-images.githubusercontent.com/43959475/196885838-3c424487-fcd5-4700-86a2-573bfdc054cf.jpg)

### docker rmi :
```bash
docker rmi sammg/welcome-app
```
![docker-rmi](https://user-images.githubusercontent.com/43959475/196885852-d1caeef6-f4f3-4bb3-a079-2254903a3e99.jpg)

---

# Task 2:

### Running [Hello World Docker Image](https://hub.docker.com/_/hello-world):

### Task Screenshots:
```bash
docker pull hello-world
docker run hello-world
```
![docker-hello-world](https://user-images.githubusercontent.com/43959475/196885901-a6fd3b5d-e736-4776-9306-b65c41072e2c.jpg)

---

# Task 3:

### Hello world fastapi application Screenshots:
```bash
docker build -t sammg/fastapi-hello .
docker run -d -p 5055:8000 sammg/fastapi-hello
docker ps -a
docker logindocker
```
![docker-fastapi-1](https://user-images.githubusercontent.com/43959475/196885952-7a3ee6eb-707f-4f06-9ebf-83c78ae17704.jpg)
![docker-fastapi-2](https://user-images.githubusercontent.com/43959475/196885994-7a74d481-3f70-4e26-860a-a1846b96cca1.jpg)
![docker-fastapi-4](https://user-images.githubusercontent.com/43959475/196886114-08bea095-10ce-45c7-8d2f-2c07f98be106.jpg)

###  Dockerfile for fastapi hello world application Screenshots:
![docker-fastapi-3](https://user-images.githubusercontent.com/43959475/196886031-6bd3dfaf-a9cc-4275-9f6f-92bf96d43ebd.jpg)

### Push docker image to DockerHub Screenshots:
![docker-fastapi-5](https://user-images.githubusercontent.com/43959475/196886153-ea3a1586-7980-4065-a728-2d4ba2df6e17.jpg)

#### Dockerhub Link for image:
https://hub.docker.com/r/sammg/fastapi-hello

---

# Task 4:

### : GH Actions for build and deploy to Dockerhub:

### Repo link:

https://github.com/Samm-G/fastapi-dockerhub-deploy

### Github Actions run and published:
![ghactions-1](https://user-images.githubusercontent.com/43959475/196886218-0e651f56-7f4e-442d-9387-291d6f761df5.jpg)


### Dockerhub Image:

https://hub.docker.com/r/sammg/fastapi-hello-auto

![ghactions-2](https://user-images.githubusercontent.com/43959475/196886231-853f85ae-2520-459f-8928-b1bb8ab061de.jpg)

---
---
<img src="https://user-images.githubusercontent.com/43959475/196886791-59b77108-a1a0-4559-b91f-ad6aa210aeba.gif" width="40%" height="40%"/>

---
---

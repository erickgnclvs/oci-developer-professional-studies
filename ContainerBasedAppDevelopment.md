# Module 2: Container-based Application Development

### What is containerization?
- This technique brings virtualization at the operational system level
- Containers have quick startup time, as booting a container takes only a fraction of a second
- Containers share the host operating system and hold only the application and related binaries

### Containerization: Benefits
- Lightweight
- Portable
- Secure

### Docker: Introduction
- Docker is an open-source project and a containerization platform
- It standardizes packaging of applications and their dependencies into containers, which share the same OS kernel
- Use Docker containers for: fast, consistent delivery of your applications and while implementing microservices and for responsive deployment and scaling

### Dockerfile
| Command    | Overview                                                |
| -------------- | ---------------------------------------------------------- |
| **FROM**       | Specify base image                                        |
| **RUN**        | Execute specified command                                 |
| **WORKDIR**    | Change current directory                                  |
| **COPY**       | Simple copy of files / directories from host to container |
| **ENV**        | Add environment variable                                  |
| **EXPOSE**     | Open designated port                                       |
| **CMD**        | Specify command at container execution (can be overwritten)|
| **ENTRYPOINT** | Specify command to execute the container                   |
| **LABEL**      | LABEL *maintainer=maintainer@mail.com* specifies the author|


### Basic Docker Commands
#### Working with docker container images

| Docker Command                                | Description                                      |
| --------------------------------------------- | ------------------------------------------------ |
| `docker image pull [IMAGE_NAME]`              | Pull an image from the Docker Hub                 |
| `docker build -f [DOCKERFILE_PATH]`           | Build an image from a Dockerfile                  |
| `docker commit [CONTAINER_NAME] [IMAGE_NAME]` | Build an image from a container                   |
| `docker tag SOURCE_IMAGE[:TAG] TARGET_IMAGE[:TAG]` | Tag a Docker image                           |
| `docker login && docker image push [IMAGE_NAME]` | Push an image to Docker Hub                   |
| `docker image ls` or `docker images`           | List container images                            |
| `docker image remove [IMAGE_NAME]` or `docker rmi [IMAGE_NAME]` | Delete an image from your system     |


### OCIR - Oracle Cloud Infrastructure Registry
**What is it?** 
- A high availability Docker v2 conttainer registry service
- Stores Dockker images in private or public repositories
- Runs as a fully managed service on OCI

**What problem does it solve?**
- Without a registry it is hard for development teams to maintain a consisten set of Docker images for 

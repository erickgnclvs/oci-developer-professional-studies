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




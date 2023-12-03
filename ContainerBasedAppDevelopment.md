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
- Without a registry it is hard for development teams to maintain a consistent set of Docker images for their containerized applications
- Without managed registry it is hard to enforce access rights and security policies for images
- It is hard to find the right images and have them  available in the region of deployment
- Container Registry is an Open Container initiative-compliant registry

**Key benefits**
- Integration
- Security
- Regional availability
- High availability
- Anywhere access

### Managing OCIR

#### Managing Repository
- Creating a repository
- Deleting a repository
- Moving repository between compartments
  
#### Managing Images
- Viewing images and image details
- Pushing/pulling images from Docker CLI
  - `docker tag project01/helloworld:latest <region-key>.ocir.io/<tenancy-namespace>/<repo-name>:<tag>`
  - `docker push <region-key>.ocir.io/<tenancy-namespace>/<repo-name>:<tag>`
  - `docker pull <region-key>.ocir.io/<tenancy-namespace>/<repo-name>:<tag>`
- Deleting and undeleting an image
- Retaining and deleting images using retention policies
  - Global retention policies
  - Custom retention policies
  >  retention: do I keep or really delete it after deleting it? default is: keep
- Untagging images (removing image)
- Pulling images from container registry during Kubernetes deployment
  - Use `kubectl`to create a Docker registry secret
  - Specify the image location in OCIR and the Docker secret in the deployment manifest file

#### Managing Security
- Policies to control repository access
  - `Allow group dev-viewerrs to inspect repos in (tenancy || compartment dev-compartment)`
  - `Allow group dev-pullers to read repos in (tenancy || compartment dev-compartment)`
  - `Allow group dev-pushers to use repos in (tenancy || compartment dev-compartment)`
  - `Allow group dev-managers to manage repos in (tenancy || compartment dev-compartment)`
- Getting and auth token
- Scanning images for vulnerabilities
  - `Allow service vulnerability-scanning-service to read repos in (tenancy || compartment dev-compartment`
  - `Allow service vulnerability-scanning-service to read comparments in (tenancy || compartment dev-compartment`

#### Preparing for Container Registry 

**Access to OCI tenancy**
> The tenancy must be subscribed to one or more of the regions in which Container Registry is available

⬇️

**Docker on local machine**
> Access to Docker CLI or Desktop to push and pull images on local machine

⬇️

**Create policy for resources**
> User must belong to a group to which a policy grants the appropriate permission or belong to the tenancy's Administrators group

⬇️

**Generate auth token**
> User must already have an OCI username and an auth token


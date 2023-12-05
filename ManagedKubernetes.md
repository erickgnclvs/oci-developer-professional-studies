# Module 3: Managed Kubernetes

### Challenges in containerization
- Failures such as container crashes
- Scheduling containers to specific machines depending on the configuration
- Upgrading or rolling back the applications
- Scaling up or down containers across a set of machines
  
### What is Kubernetes?
- Kubernetes is an open source and portable platform
- It is a container orchestration tool, which automates scaling of workloads
- It groups containers into logical units

> Master node -> worker nodes -> pods -> containers

**Kubernetes can:**
- Run containerized applications of any scale without any down time
- Self-heal containerized applications
- Greatly simplifies deployment operations

>  **Docker** is used to manage and build the containers
> 
>  **Kubernetes** links containers running on multiple hosts and orchestrates them
> 
>  **Containers** communicate with each other via Kubernetes

### Container Engine for Kubernetes - OKE: Overview

**Core**
> Fully managed, scalable and highly available service

**Engine**
> Uses the open-source system: Kubernetes

**Creation**
> Define and create OKE clusters using:
> - Console
> - REST API

**Access**
> Access clusters using:
> - `kubectl`
> - Kubernetes Dashboard
> - Kubernetes API

### OKE: When and Why
**Use OKE when it's**
- Too complex, costly and time consuming to build and maintain Kubernetes environments
- Too hard to integrate Kubernetes with a registry and build process for container lifecycle management
- Too dificult to manage and control team access to production clusters

**Key benefits**
- Enables developers to get started and deploy containers quickly
- Gives DevOps teams visibility and control for Kubernetes management
- Combines production grade container orchestration of open Kubernetes with control, security, IAM, and highly predictable perormance of Oracle's next generation cloud infrastructure

### Supported Shapes and Operating Systems
#### Shapes
- Flexible shapes
- Bare metal shapes
- Standard & GPU shapes
- HPC shapes (except in RMA networks)
- Dense I/O shapes
- ~Bare metal HPC shapes with RDMA~
- ~Micro VM shapes~
- ṼM.Standard.ER.Flex~

#### Operating Systems
- Most Oracle Linux
- Custom images (based on supported Oracle Linux)

> Query supported shapes and images
> 
> `oci ce node-pool-options get --node-pool-option-id all`

#### Supported Kubernetes Versions
##### Operating systems
- 3 versions supported at all times for new clusters
- WHen new versions are added, the oldest is supported for **at least 30 days**

### Prerequesite to Create an OKE Cluster
- Access to an OCI tenancy
- Sufficient quota on resource - service limits
- Ready-to-deploy compatment
- Configuring network resources
- Policies
- Tools: kubectl and KubeConfig

### Network Resource Configuration for Clster Creation and Deployment

### Version Drift in Control Plane Nodes and Worker Nodes
- Kubernetes version on worker nodes can be as recent as that on the control plane
- Versions on the worker nodes can lag behind the control plane by up to two minor versions

### Creating OKE Cluster on OCI

#### Quick Create Workflow
- Use defaults where possible
- Network resources are created automatically
- Options include:
  - Kubernetes version
  - API endpoint visibility
  - Node shape, number
  - Image verification

#### Custom Create Workflow
- There are more options to customize
- Use existing networking resources
- Create a cluster with no node pools or add node pools later
- Options include:
  - Secrets encryption
  - Pod security policies
  - NSGs for security
  - Custom CIDR blocks for pods and services
  - Node placement
  
#### API Driven/Automation
- Maximum customization
- Leverage APIs/SDKs/Terraform
- Options include:
  - Custom images for worker nodes

### The Art of Designing Your Cluster
- Node types
- Workload characteristics
- Operational considerations 
- Cost optimization and scaling

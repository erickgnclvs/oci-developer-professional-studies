# Module 1: Cloud Native Fundamentals

- DevOps
- Kubernetes
- Docker
- Serverless Functions
- API's
- Stream Processing with Kafka

### Why Cloud Native?
- **Enhanced customer experience**
  - Facilitate frequent changes
  - Robustly develop and deliver solutions
  - Written, tested and deployed on the cloud
  - Operational efficiency
 
- **Cost effectiveness**
  - Convert capital expenditure into operational expenditure
  - Management and monitoring tools being used

- **Ease of management**
  - Provides a useful app development process
  - Empower the corporate teams

- **Digital transformation with better security measures and analytics**

### Cloud-Native, Cloud-Enabled and Cloud-Based Applications
- Cloud-Native systems are constructed in the cloud from scratch to harness the power of popular public cloud environments
- Cloud-Enabled applications is an application that has been moved to the cloud but was originally developed for use in a conventional data center
- Cloud-Based is the middle ground between Cloud-Native and Cloud-Enabled

### Cloud-Native versus Cloud-Based Applications

| Characteristic   |      Cloud-Native Applications      |  Cloud-Based Applications |
|----------|-------------|-------|
| **Origin** |  Built and deployed in the cloud, truly accessing the power of cloud infrastructure | Made in house using legacy infrastructure and tweaked to be made remotely available in the cloud |
| **Design** |    Designed to be hosted as multi-tenant instances   |   Made on in-house servers; Don't have multi-tenant instances |
| **Ease of Use** | Flexible and built to scale and areas of an app can be upgraded without disruption |    Require manual upgrades, causing distruption and shutdown to the application |
| **Pricing** | Cheaper |   More expensive |
| **Maintenance** | interruptions are limited because of the microservice architecture |   Interruptions can occur because of hardware migration or specialized software configurations |

### Key Pillars of Cloud Native Development

> **What is CNCF?**
>   - CNCF is an open-source software foundation dedicated to making cloud-native computing universal and sustainable
>   - Kubernetes, Fluentd, Envoy, Prometheus, CoreDNS, Helm, Hardbor, ContainerD, ETCD, Vitess
 
#### Microservices
- Enable you to design your application as a collection of loosely coupled services

#### Containers
- Containers are packages of software that contain all the necessary elements to run in any environments

#### DevOps
- Combination of development and operations brought together to crreate a unified infrastructure designed to maximize productivity

#### CI/CD
- A CI/CD pipeline automates your software delivery process. This helps developers merge and test code more frequently

#### Service Mesh
- A service mesh is a configurable, low-latency infrastructure layer that controls the interaction between a network of microservices

### Benefits of Cloud Native Development
- Faster release
- Ease of management
- Reduced cost
- Reliable system
- Avoid vendor lock-in
- Scalability
- Auto-provisioning

### Challenges of Cloud Native Development
- Complex architecture
- Latest technology enhancements
- Continuous innovation
- Over-dependence on a platform or provider
- Skills shortage
- Security
- High operational and technology costs

### Microservices Architecture: Overview
> **What are microservices?**
>   - Lightweight services that do a task very well and only that task
>   - REST API
>   - Multilingual
>   - Loosely coupled with other services
>   - Easy to maintain and independently deployable
>   - Easily scalable and highle available
>   - Failures resistant

### Microservices versus Monolithic Architectures
| Characteristic   |      Microservices Architecture      |  Monolithic Architecture |
|----------|-------------|-------|
| **Unit design** |  Loosely coupled services | Single unit |
| **Functionality reuse** |  Microservices defin APIs that expose their functionality to any client | Limited |
| **Communication within the application** |  REST API calls based on the HTTP protocol | Internal procedures (function calls) |
| **Technological flexibility** |  Developed using a programming language and framework that best suits the problem | Written in a single programming language |
| **Data management** |  Decentralized | Centralized |
| **Deployment** |  Independently | Any minor change requires redeployment |
| **Maintainability** |  Easier to maintain | Complex to maintain |
| **Resiliency** |  High | Low |
| **Scalability** |  Each microservice can be scaled independently | The entire application needs to be scaled |

### Design Methodology of Microservices
> **12-Factor Methodology for Developing Microservices-based Applications**
>   - Codebase
>   - Dependencies
>   - Configuration
>   - Backing services
>   - Build, release and run
>   - Processes
>   - Port binding
>   - Concurrency
>   - Disposability
>   - Development and production parity
>   - Logs
>   - Admin processes

### Microservices Designs: Benefits
- Easier to build and maintain apps
- Organized around business capabilities
- Improved productivity and speed of deployment
- Increased fault tolerance and fault isolation
- Greater scalability and flexibility
- Simplified security monitorin
- Autonomous, cross-functional teams

### Microservices Designs: Drawbacks
- More complex
- More expensive than monoliths
- Require cultural changes
- Present harder debugging problems
- Present security threats

  

# **Cloud Computing Compute Services Notes**

Compute in cloud computing refers to the processing power and memory resources provided by a cloud service provider (CSP) to run applications, execute workloads, and process data. It's the engine that runs everything in the cloud.

These resources are virtualized, allowing users to rent and scale them on-demand without managing the underlying physical hardware.

---

1. **Key Compute Concepts**

**Compute Resources**:	Hardware and software needed for computation: CPU, RAM (Memory), Storage, and Networking. Sometimes includes GPUs for intensive tasks like Machine Learning.

**Virtualization**:	The core technology that divides physical hardware (servers) into multiple isolated, virtual environments (VMs or instances). This allows for efficient resource sharing.

**Instance**:	The smallest unit of compute resources you can rent, typically a Virtual Machine (VM) or a container. Instances come in different types (General Purpose, Compute Optimized, Memory Optimized, etc.).

**Elasticity/Scalability**:	The ability to automatically scale compute capacity up (add resources) or down (remove resources) quickly in response to changing demand, ensuring optimal cost and performance.

---

2. **Main Cloud Compute Service Models**

The way compute is provided is primarily categorized under the three main Cloud Service Models (IaaS, PaaS, and FaaS/Serverless), which dictate the level of management control you maintain.

_**Models, focus and User Management Responsibility**_

- **Infrastructure as a Service (IaaS)**:	Virtual Servers (VMs)
    -     Operating System (OS), Middleware, Applications, Data, Runtime.	AWS EC2, Azure Virtual Machines, Google Compute Engine (GCE)

- **Platform as a Service (PaaS)**:	Application Development Environment
    -     Applications, Data.	AWS Elastic Beanstalk, Azure App Service, Google App Engine (GAE)

- **Function as a Service (FaaS) / Serverless**:	Running Code (Functions)
    -     Code/Functions (The code to run).

---

3. **Core Compute Service Types (Across all Major CSPs)**

   _**A. Virtual Machines (IaaS)**_

    Description: The user rents a virtual server (an Instance) with a choice of OS, CPU, RAM, and storage. It provides the most control over the environment.

       Key Services:

          AWS: Amazon EC2 (Elastic Compute Cloud)
  
          Azure: Azure Virtual Machines
  
          Google Cloud: Google Compute Engine (GCE)

    Use Cases: Hosting traditional enterprise applications, running custom operating systems, lifting and shifting existing on-premises workloads.

  _**B. Containers (PaaS/IaaS)**_

  Description: An application is packaged with its dependencies into a lightweight, portable Container (e.g., Docker). Containers run in isolated environments and share the host OS kernel, making them faster to start and more resource-efficient than VMs. Orchestration services manage the deployment, scaling, and networking of these containers.

    Key Services (Orchestration):

        AWS: ECS (Elastic Container Service) and EKS (Elastic Kubernetes Service)

        Azure: Azure Kubernetes Service (AKS) and Azure Container Instances

        Google Cloud: Google Kubernetes Engine (GKE) (Kubernetes was originally developed by Google)

  Use Cases: Microservices architecture, CI/CD pipelines, modernizing existing applications.

_**C. Serverless Computing (FaaS)**_

  Description: The user only uploads their code (a Function), and the cloud provider automatically manages the entire underlying infrastructure, including provisioning, scaling, and patching. You pay only when your code is running (event-driven execution).

    Key Services:

        AWS: AWS Lambda

        Azure: Azure Functions

        Google Cloud: Google Cloud Functions

  Use Cases: Event processing (e.g., responding to a file upload), building simple APIs, processing data streams.

---

4. **Key Benefits of Cloud Compute Services**

 - **Cost Efficiency (Pay-as-you-go)**: Eliminate capital expenditure on hardware and pay only for the compute resources consumed.

 - **Agility & Speed**: Provision resources in minutes instead of weeks or months. Developers can quickly set up development and testing environments.

 - **High Availability & Reliability**: Services run on a global network of secure data centers with redundancy and automatic failover capabilities.

 - **Reduced Operational Overhead**: The cloud provider handles the "undifferentiated heavy lifting" like physical server maintenance, power, cooling, and network infrastructure.


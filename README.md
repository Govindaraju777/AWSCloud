# AWSCloud
my notes on aws cloud 

# Hypervisor
    In order to start creating virtual machines, you need a hypervisor.

    A hypervisor, or virtual machine monitor (VMM) is a software layer between the host machine, the physical server, and the guest machines, the virtual machines. 
    It interacts with hardware and provides an interface to share the available resources with the guest operating systems.

https://www.vmware.com/topics/glossary/content/bare-metal-hypervisor.html

    What is meant by bare metal?
    The term bare metal refers to the fact that there is no operating system between the virtualization software and the hardware. The virtualization software resides on the “bare metal” or the hard disk of the hardware, where the operating system is usually installed. 

    Bare metal isn’t only used to describe hypervisors. A bare metal server is a regular, single-tenant server. However, it can be a host machine for virtual machines with the addition of a hypervisor and virtualization software. A bare metal cloud refers to a customer renting the actual servers that host the public cloud from a cloud service provider, in addition to renting the public cloud services. 
    What is the difference between bare metal hypervisors and hosted hypervisors?
    The bare metal hypervisor is the most commonly deployed type of hypervisor. This is where the virtualization software is installed directly on the hardware, where the operating system is normally installed. Bare metal hypervisors are extremely secure since they are isolated from the attack-prone operating system. They perform better and more efficiently than hosted hypervisors, and most companies choose bare metal hypervisors for enterprise and data center computing needs. 


    There is another type of hypervisor, known as a client or hosted hypervisor. While bare metal hypervisors run directly on the computing hardware, hosted hypervisors run within the operating system of the host machine. Although hosted hypervisors run within the OS, additional operating systems can be installed on top of it. Hosted hypervisors have higher latency than bare metal hypervisors because requests between the hardware and the hypervisor must pass through the extra layer of the OS. Hosted hypervisors are also known as client hypervisors because they are most often used with end users and software testing, where the higher latency is not as much of a concern. 
    
    

# What is cloud compuring 
  Cloud computing is a remote virtual pool of on-demand shared resources offering Compute, Storage, and Network services that can be rapidly deployed at scale.

  https://cloudacademy.com/blog/what-is-cloud-computing/
  

## Cloud Deployment models
1. Public 2. Private 3. Hybrid

<img width="1680" alt="Screenshot 2021-12-23 at 11 08 32 PM" src="https://user-images.githubusercontent.com/17598334/147274921-02e5e59f-fbb0-49c7-bdb7-7f422243ecdb.png">

# AWS cloud compute Index
https://aws.amazon.com/products/compute/
<img width="1657" alt="Screenshot 2021-12-27 at 12 19 35 AM" src="https://user-images.githubusercontent.com/17598334/147417369-f9ad1bba-305a-453b-8f7a-f90fd86aeb19.png">


# AWS ECS Vs. EKS Vs. Fargate: Which One Should You Use?
https://www.cloudzero.com/blog/ecs-vs-eks
### Amazon ECS vs. EKS: What Are The Best Use Cases?
### Amazon Fargate for ECS Or EKS: What Is It?
        AWS Fargate is a serverless compute service for containers that can be used to run both Amazon ECS and EKS. Both services (ECS and EKS) manage how your containers run, but you still need a compute layer.

<img width="1633" alt="Screenshot 2021-12-27 at 5 10 14 PM" src="https://user-images.githubusercontent.com/17598334/147468554-e4ede33e-709a-489e-aaee-f2c3e85f099c.png">


# Elastic Load Balancing features
https://aws.amazon.com/elasticloadbalancing/features/

# Listener rules for your Application Load Balancer
https://docs.aws.amazon.com/elasticloadbalancing/latest/application/listener-update-rules.html

# AWS S3 Storage Classes
<img width="1288" alt="Screenshot 2022-01-04 at 7 44 49 PM" src="https://user-images.githubusercontent.com/17598334/148072019-f973dbae-1b3a-4b4d-98e7-4d709df8b665.png">

<img width="1532" alt="Screenshot 2022-01-09 at 9 56 15 PM" src="https://user-images.githubusercontent.com/17598334/148691180-da3d80ef-1df2-4b17-849a-31d797e56b69.png">


# S3 , EBS, EFS
<img width="1290" alt="Screenshot 2022-01-04 at 10 25 36 PM" src="https://user-images.githubusercontent.com/17598334/148094961-8999d3c3-e023-43fb-bab3-e74b082395d7.png">

# Selecting the right database in Amazon Web Service(AWS)
![image](https://user-images.githubusercontent.com/17598334/148815513-1af21a1c-7313-4e96-929e-e80c51b98a03.png)


## Amazon Web Services (AWS) provides several services that can be used to run Docker containers. Here are some of the key AWS services for running Docker images:
    
    Amazon Web Services (AWS) provides several services that can be used to run Docker containers. 
    
Here are some of the key AWS services for running Docker images:
    
### Amazon Elastic Container Service (ECS):
    
    Description: A fully managed container orchestration service that allows you to run Docker containers without managing the underlying infrastructure.
    Use Cases: Microservices, batch processing, and long-running applications.
    
    
### Amazon Elastic Kubernetes Service (EKS):
    
    Description: A managed Kubernetes service that simplifies the deployment, management, and scaling of containerized applications using Kubernetes.
    Use Cases: Complex containerized applications requiring the flexibility and power of Kubernetes.

### AWS Fargate:
    
    Description: A serverless compute engine for containers that allows you to run containers without managing the underlying infrastructure. You only pay for the vCPU and memory allocated to your containers.
    Use Cases: Short-lived, stateless containers, and applications with varying workloads.

### Amazon EC2 Container Service (deprecated, replaced by ECS and Fargate):
    
    Description: The predecessor to ECS, provided a way to run Docker containers on EC2 instances.
    Note: While EC2 Container Service is still mentioned in some documentation, AWS recommends using ECS or Fargate for new containerized applications.

#### AWS Batch:
    
    Description: A fully managed service for running batch computing workloads. While not specifically for Docker containers, it supports containerized applications and can be used for running Docker images in batch processing scenarios.
    Use Cases: Batch processing, data processing, and scientific computing.

#### AWS Lambda (with AWS Lambda Layers for Container Images):
    
    Description: 
    While traditionally used for serverless functions, AWS Lambda has introduced support for container images. 
    You can package and deploy your application as a container image and run it using Lambda.
    Use Cases: Short-lived, event-driven functions, and applications with unpredictable workloads.
    When choosing a service, consider factors such as the level of abstraction, ease of management, flexibility, and scalability based on the specific requirements of your application. 
    ECS and EKS are particularly well-suited for more complex containerized applications, while Fargate provides a serverless option for simplified management.

#### Infra automation tools
    AWS CloudFormation, Terraform, Chef, Puppet, and Azure Automation are all tools and services used in the realm of infrastructure automation and configuration management, but they serve different purposes and have distinct features. Here's a brief comparison:

1) AWS CloudFormation:

    Provider: AWS-specific.
Purpose: Infrastructure as Code (IaC) for AWS resources.
Description: AWS CloudFormation allows you to describe and provision AWS infrastructure resources in a declarative template.
It's native to AWS and tightly integrated with its services. You define your infrastructure in a JSON or YAML template, and CloudFormation handles the provisioning and management of resources.

2) Terraform:

    Provider: Multi-cloud (supports AWS, Azure, Google Cloud, and others).
    Purpose: Infrastructure as Code for multiple cloud providers.
    Description: Terraform is a popular open-source tool that supports a multi-cloud approach. It uses a declarative language (HCL) to define infrastructure, and it provides a consistent workflow for provisioning and managing resources across various cloud providers. Terraform is known for its flexibility and extensibility.

3) Chef:

    Provider: Cross-platform (supports both on-premises and cloud environments).
    Purpose: Configuration management and automation.
    Description: Chef is a configuration management tool that automates the process of configuring and managing servers. It uses a Ruby-based language to define configurations (recipes) and supports a client-server architecture.
   Chef is platform-agnostic and can be used in both on-premises and cloud environments.

4) Puppet:

    Provider: Cross-platform.
    Purpose: Configuration management and automation.
    Description: Puppet is another configuration management tool that uses a declarative language to define configurations (manifests). It operates on a client-server model and is designed to manage the configuration of servers in a consistent and scalable way. Puppet is cross-platform and supports a wide range of operating systems.


5) Azure Automation:

    Provider: Azure-specific.
    Purpose: Automation and configuration management for Azure resources.
    Description: Azure Automation is a service provided by Microsoft Azure for automating the creation, deployment, and management of Azure resources. It supports the use of PowerShell and graphical runbooks for defining automation workflows. It is tightly integrated with Azure services.
In summary, AWS CloudFormation and Azure Automation are specific to AWS and Azure, respectively, while Terraform is a multi-cloud IaC tool. Chef and Puppet are more focused on configuration management and can be used in diverse environments, including on-premises and various cloud providers. The choice between these tools often depends on specific use cases, existing infrastructure, and team preferences.
    

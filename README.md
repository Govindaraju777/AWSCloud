# AWSCloud
my notes on aws cloud 

# Hypervisor
    In order to start creating virtual machines, you need a hypervisor.

    A hypervisor, or virtual machine monitor (VMM) is a software layer between the host machine, the physical server, and the guest machines, the virtual machines. It interacts with hardware and provides an interface to share the available resources with the guest operating systems.

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

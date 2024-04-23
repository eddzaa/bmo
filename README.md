# Custom WooCommerce-Based Product Deployment

## Exercise Description

The Application Engineering team has been developing a custom WooCommerce-based product that needs to be deployed for an initiative. As a member of the DevOps Engineering team, your task is to create the cloud-based infrastructure to support this deployment. You will need to create a reference architecture and implement it using modern Infrastructure as Code (IaC) techniques with documentation for a 3-tier application. You can utilize serverless or container technology or virtual machines (VMs) for implementation. Candidates are required to push the code to GitHub using IAC (Infrastructure as Code) – CDK (Cloud Development Kit).

## Task Requirements

1. Create a reference architecture for a 3-tier application.
2. Implement the architecture using modern Infrastructure as Code (IaC) techniques.
3. Provide documentation for the implemented solution.
4. Push the code to GitHub.

## Solution Overview

### Solution Architect Diagram

![Three-tier Application Solution Architect Diagram]:<img src="https://github.com/eddzaa/eddzaa/bmo/solution architect diagram.png">

This architecture follows a three-tier web application pattern with separation of concerns:

    Networking Tier: A VPC with public and private subnets, an internet gateway, NAT gateway, and routing tables.
    Web Tier: An Application Load Balancer, an Auto Scaling group with web servers, and security groups. The web servers run  application that interacts with the database.
    Database Tier: A MySQL database instance in the private subnet, with a security group allowing traffic from the web tier.

The web servers are launched in the public subnets and can receive traffic from the internet via the Load Balancer. The database instance is in the private subnet for security reasons and can only be accessed from the web tier.

#### Architecture Components:
**Tier 1: Presentation Layer**
- This layer represents the user interface and interaction layer.
- It includes components responsible for presenting information to the users and collecting user inputs.
- In the provided directory structure, this could correspond to the `compute` module where the main application code resides.

**Tier 2: Application Layer**
- This layer contains the application logic and processing.
- It handles the business logic, data manipulation, and other application-specific tasks.
- In the provided directory structure, this could correspond to the `database` module where the database-related configuration and logic reside.

**Tier 3: Data Layer**
- This layer manages the data storage and retrieval.
- It includes databases, data storage systems, and other data-related components.
- In the provided directory structure, this could correspond to the `networking` module where the network-related configurations such as load balancers and networking components are defined.

This architecture separates concerns and provides a modular structure for building and managing the application components.


Thank you for considering my submission for the cloud-based infrastructure exercise. I have implemented a three-tier application architecture using modern Infrastructure as Code (IaC) techniques, leveraging AWS resources. The provided solution architect diagram and directory structure demonstrate the modularity and scalability of the infrastructure design.

I am excited about the opportunity to discuss my implementation further in the upcoming interview sessions. Please feel free to reach out if you have any questions or need further clarification on any aspect of the solution.







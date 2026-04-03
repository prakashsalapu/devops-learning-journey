# 06 - AWS VPC

This module introduces AWS VPC, which is one of the core networking components in Amazon Web Services. If you plan to work in DevOps, cloud engineering, or solutions architecture, you must understand VPC clearly. Every cloud resource you create will live inside a VPC.

## What is a VPC

A VPC is a Virtual Private Cloud. It is your own isolated network inside AWS. You control everything inside it, including IP ranges, subnets, routing, security, and traffic flow. Think of it as your private data center inside the AWS cloud.

## Key Parts of a VPC

### CIDR Block  
A CIDR block defines the IP range of your VPC.  
Example: 10.0.0.0/16  
This gives you sixty five thousand five hundred thirty four usable IP addresses.  
You must choose this range carefully because all subnets will come from this pool.

### Subnets  
Subnets divide your VPC into smaller networks.  
Two types of subnets exist:

- Public subnet, resources here have internet access  
- Private subnet, resources here stay internal and secure  

Public subnets usually hold load balancers or NAT Gateways.  
Private subnets hold servers, databases, and internal applications.

### Route Tables  
Route tables define how traffic flows inside the VPC.  
Examples:  
- Public route table routes traffic to an Internet Gateway  
- Private route table routes traffic to a NAT Gateway  

Each subnet must be associated with a route table.

### Internet Gateway  
This allows communication between your VPC and the internet.  
Attach it to the VPC and update the route table for public subnets.

### NAT Gateway  
This allows instances in private subnets to access the internet for updates or package downloads.  
It prevents external systems from initiating connections back to those instances.

### Security Groups  
Security groups act as virtual firewalls for instances.  
They allow or block traffic based on ports and protocols.  
They operate at the instance level.

### Network ACLs  
Network ACLs provide traffic control at the subnet level.  
They allow and deny rules and apply to all resources inside the subnet.

## How Traffic Works in a VPC

A typical pattern looks like this:

- Public subnet contains a load balancer  
- Private subnet contains EC2 instances  
- The load balancer routes requests into the private subnet  
- Outbound traffic from private instances goes through a NAT Gateway  
- Public subnet uses an Internet Gateway for global access  

This structure improves security and reduces attack surface.

## Common VPC Designs for Beginners

### Single Public Subnet Setup  
Used for small test projects.  
Limitations: bad for production because everything is exposed.

### Public and Private Subnet Setup  
Most common beginner friendly production pattern.  
Public subnet hosts load balancers or NAT.  
Private subnet hosts servers and databases.

### Multi Availability Zone Setup  
Used for high availability.  
You create multiple subnets across different zones.  
Traffic continues even if one zone fails.

## Why VPC Matters in DevOps

You will use VPC every day when working with:

- EC2 instances  
- RDS databases  
- Load balancers  
- EKS and Kubernetes clusters  
- S3 VPC endpoints  
- Lambda functions inside private networks  

Misconfiguring a VPC leads to outages, blocked traffic, unreachable services, and security risks. Understanding how subnets, route tables, gateways, and security groups work is mandatory.

## Summary

- A VPC is your own isolated cloud network  
- You define IP ranges using CIDR blocks  
- Subnets divide your VPC into public and private parts  
- Route tables manage traffic flow  
- Internet Gateway gives internet access to public subnets  
- NAT Gateway gives secure outbound access to private subnets  
- Security groups and NACLs protect your resources  
- VPC knowledge is essential for real cloud and DevOps work  

Practice by creating your own VPC, adding subnets, attaching gateways, and testing routes. This builds real confidence and prepares you for production level networking.

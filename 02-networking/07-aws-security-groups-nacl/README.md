# 07 - AWS Security Groups and NACL

This module explains two important AWS networking security tools. Security Groups and Network ACLs control traffic in a VPC. Many beginners confuse them, but they behave very differently. If you do not understand this, you will face random connectivity failures in EC2, RDS, EKS, and load balancers.

## What Are Security Groups

A Security Group is a virtual firewall that works at the instance level. It controls which traffic is allowed to enter or leave a specific resource.

### Key Points  
- Security Groups are stateful  
- If inbound traffic is allowed, the return traffic is automatically allowed  
- You must explicitly allow inbound rules  
- Outbound rules are open by default  
- Security Groups are attached to resources like EC2, RDS, and load balancers  

Stateful means AWS remembers the connection. Once the incoming traffic is allowed, the response does not need another outbound rule.

### Common Use Cases  
- Allow SSH on port 22 for administrators  
- Allow HTTP or HTTPS for web servers  
- Allow database access only from application servers  
- Block everything else to keep the environment secure  

Security Groups keep individual resources safe.

## What Are Network ACLs

A Network ACL is a firewall that works at the subnet level. It affects all resources inside the subnet.

### Key Points  
- NACLs are stateless  
- Both inbound and outbound rules must be written  
- They allow and deny rules  
- They operate at the subnet boundary  
- Every subnet must have one NACL  

Stateless means AWS does not remember the connection. If you allow inbound traffic on a port, you must also allow outbound traffic for the return packet.

### Common Use Cases  
- Allow only specific IP ranges into a subnet  
- Block suspicious IP addresses  
- Enforce stricter controls for sensitive subnets  
- Provide an extra security layer along with Security Groups  

NACLs control traffic at a broader network level.

## Security Group vs NACL

Understanding the differences helps you select the right tool.

### Security Groups  
- Stateful  
- Allow rules only  
- Used at instance level  
- Simpler to manage  
- Commonly used for most configurations  

### NACLs  
- Stateless  
- Allow and deny rules  
- Applied at subnet level  
- More strict and detailed  
- Used for advanced or layered security setups  

Security Groups act as the primary defense. NACLs act as an outer protective layer.

## Practical Examples

### Example 1  
You want to allow SSH only for your IP.  
Use a Security Group inbound rule:  
- Allow TCP, port 22, source your IP

### Example 2  
You want to block an entire IP range from accessing a subnet.  
Use a NACL inbound deny rule.

### Example 3  
Your private subnet EC2 instances must call the internet through NAT.  
You need the correct outbound rules in the NACL and security group.

### Example 4  
A load balancer in a public subnet accepts port 443 from anywhere.  
The EC2 instances behind it accept port 443 only from the load balancer Security Group.

Without this separation, your architecture becomes insecure.

## How These Apply in DevOps

You will configure Security Groups and NACLs in tasks such as:

- EC2 deployment  
- RDS database access  
- EKS node security  
- Load balancer setup  
- VPC subnet isolation  
- CI CD runners in private networks  

Most connectivity issues in AWS are caused by wrong rules in either a Security Group or a NACL. You must know where to look and what to fix.

## Summary

- Security Groups protect individual resources and are stateful  
- NACLs protect subnets and are stateless  
- Security Groups use allow rules  
- NACLs use allow and deny rules  
- Both tools are essential for building secure AWS architectures  

Test these by creating a VPC, adding subnets, using different rules, and observing how traffic behaves. This hands on practice strengthens your understanding and makes you confident with AWS networking operations.

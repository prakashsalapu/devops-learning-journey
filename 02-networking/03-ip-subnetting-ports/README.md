# 03 - IP Addressing, Subnetting, and Ports

This module explains three networking basics that every DevOps beginner must understand. These concepts appear everywhere in cloud, containers, Kubernetes, and server setups. Learn them properly now, or you will get stuck later.

## IP Addressing

An IP address is like a home address for a device on a network. It tells the network who the device is and how to reach it. Every IP has two parts.  
1. Network part  
2. Host part  

### IPv4  
This is the older and most commonly used version.  
Format: A.B.C.D  
Example: 192.168.1.10  
IPv4 has 2^32 total addresses.

### IPv6  
This is the newer version with a massive number of addresses.  
Format: eight groups of hexadecimal values  
Example: 2001:db8:85a3:0000:0000:8a2e:0370:7334  
IPv6 has 2^128 total addresses and fixes the shortage of IPv4.

## Subnetting

Subnetting is the process of splitting one big network into smaller parts. This helps organize networks, control traffic, and improve security. Cloud platforms like AWS, Azure, and GCP heavily rely on subnetting.

### CIDR Notation  
CIDR tells how many bits are used for the network portion.  
Example: 192.168.1.0/24  
Here, /24 means the first 24 bits are the network part.

### What You Should Be Able to Calculate  
If you understand subnetting, you can find:  
- Total hosts in the network  
- Network address  
- Broadcast address  
- First usable and last usable IP  

Example for /24  
- Hosts: 2^(32 minus 24) minus 2 = 254  
- Network address: 192.168.1.0  
- Broadcast address: 192.168.1.255  

### Common Subnets  
- /30 gives only 2 usable hosts  
- /29 gives 6 usable hosts  
- /24 gives 254 usable hosts  
- /16 gives a large network used in cloud VPCs  

Subnetting is important because it helps divide and manage large networks in a structured way.

## Ports and Protocols

If an IP address identifies a device, a port identifies a specific application inside that device. Think of a port as a door in a house. The house is the IP, and the door is the port.

### Port Ranges  
- 0 to 1023: well known ports  
- 1024 to 49151: registered ports  
- 49152 to 65535: temporary or dynamic ports  

### Common Ports Beginners Must Know  

| Service | Protocol | Port |
|--------|----------|------|
| SSH | TCP | 22 |
| HTTP | TCP | 80 |
| HTTPS | TCP | 443 |
| DNS | UDP,TCP | 53 |
| FTP | TCP | 20,21 |
| SMTP | TCP | 25 |
| MySQL | TCP | 3306 |
| PostgreSQL | TCP | 5432 |

These ports show up constantly in DevOps tasks, so memorize them.

### Why Ports Matter  
Ports are used in:  
- Docker container port mapping  
- Kubernetes service communication  
- Cloud security groups and firewall rules  
- Load balancer configurations  

Without understanding ports, you will struggle with almost every DevOps tool.

## Summary

- IP addresses identify devices on a network  
- Subnetting divides networks into smaller parts for better management  
- Ports identify applications running on a device  
- These concepts form the foundation of real DevOps work  

Take time to practice calculating subnets and identifying ports. These basics will make advanced DevOps topics much easier to understand.

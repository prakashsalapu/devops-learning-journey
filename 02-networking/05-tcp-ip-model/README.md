# 05 - TCP IP Model

This module explains the TCP IP Model in a simple, beginner friendly way. The TCP IP Model is the real world networking model used by the internet and all modern systems. Cloud platforms, servers, Kubernetes clusters, containers, and routers all follow this model for communication.

## What is the TCP IP Model

The TCP IP Model describes how data moves across a network from one device to another. It is simpler than the OSI Model and actually used in real networking. It has four layers.

1. Application  
2. Transport  
3. Internet  
4. Network Access  

Each layer has specific responsibilities that help devices communicate reliably.

## Layer by Layer Explanation

### Application Layer  
This layer deals with network applications and protocols that users interact with. It combines the top three layers of the OSI Model.  
Examples of protocols:  
- HTTP and HTTPS for web  
- DNS for domain names  
- FTP for file transfers  
- SMTP for email  

Any service or application that communicates over a network works at this layer.

### Transport Layer  
This layer controls how data moves between devices. It ensures proper delivery, sequencing, and error checking when needed.  
Main protocols:  
- TCP for reliable communication  
- UDP for fast, connectionless communication  

TCP guarantees delivery. UDP focuses on speed.

### Internet Layer  
This layer deals with addressing and routing. It decides the best path for packets through different networks.  
Main protocols:  
- IP for addressing  
- ICMP for error reporting and diagnostics  
- ARP for mapping IP to MAC addresses  

Routers work primarily at this layer.

### Network Access Layer  
This layer handles how data is physically transmitted in a local network. It includes the hardware and low level protocols.  
Examples:  
- Ethernet  
- WiFi  
- MAC addressing  
- Switching  

This layer is responsible for delivering data inside the same network segment.

## TCP IP vs OSI Model for Beginners

The OSI Model has seven layers.  
The TCP IP Model has four layers and is the practical model used in real life.

Mapping for reference:

- Application in TCP IP covers Application, Presentation, Session in OSI  
- Transport in TCP IP matches Transport in OSI  
- Internet in TCP IP matches Network in OSI  
- Network Access in TCP IP covers Data Link and Physical in OSI  

Understanding this mapping helps you relate both models easily.

## Why the TCP IP Model Matters in DevOps

You will use this model constantly while working with:

- Docker port mappings  
- Kubernetes services and networking  
- VPC subnets and routing  
- Firewalls and security groups  
- Load balancers  
- DNS setups  
- Server to server communication  

When something breaks, knowing which layer to analyze saves time.

Examples:

- DNS failure is at Application layer  
- Port issues often belong to Transport layer  
- Routing issues belong to Internet layer  
- LAN connection issues belong to Network Access layer  

This knowledge helps you troubleshoot accurately instead of guessing.

## Summary

- The TCP IP Model has four layers and is used by real networks and the internet  
- Application layer handles user level protocols  
- Transport layer handles TCP and UDP communication  
- Internet layer handles addressing and routing  
- Network Access layer handles local network communication  

Master the TCP IP Model because every cloud, DevOps, and networking tool you use is built on top of it.

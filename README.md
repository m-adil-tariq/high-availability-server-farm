# High Availability Web Server Network Using Dynamic Routing, Load Balancing, and Failover

> **Documentation:** For network topology diagrams, implementation screenshots, configuration details, IP addressing tables, OSPF configurations, testing results, and performance analysis, please refer to the accompanying **[Project Report](Project%20Report.pdf)**.

<img width="1920" height="1080" alt="image (9)" src="https://github.com/user-attachments/assets/4449e6fe-dd22-41c4-a3c7-2e2d000e4821" />

## Overview

This project demonstrates the design and implementation of a **High Availability (HA) Web Server Network** using dynamic routing, redundant network paths, and load balancing techniques. The network is designed to ensure continuous web service availability by eliminating single points of failure and automatically rerouting traffic when failures occur.

The simulation was developed in Cisco Packet Tracer and focuses on enterprise-grade concepts such as OSPF routing, Equal-Cost Multi-Path (ECMP) load balancing, and network failover mechanisms.

---

## Problem Statement

Traditional network architectures often depend on a single server and a single communication path. Such designs suffer from:

* Single Points of Failure (SPOF)
* High downtime during network failures
* Manual recovery procedures
* Poor scalability
* Network bottlenecks under heavy traffic

This project addresses these issues by implementing a resilient and redundant network infrastructure capable of maintaining service availability even when links or devices fail.

---

## Objectives

* Design a redundant network topology with multiple routing paths.
* Implement OSPF dynamic routing for automatic route discovery and failover.
* Utilize Equal-Cost Multi-Path (ECMP) routing for traffic distribution.
* Eliminate single points of failure between clients and servers.
* Simulate and test failover scenarios.
* Analyze network performance using ping and traceroute tests.

---

## Network Architecture

The network follows a three-tier architecture:

### 1. Access Layer

* Client PCs
* Printer
* DNS Server
* LAN Switch

### 2. Core / Transit Layer

* Multiple interconnected routers
* Redundant communication paths
* OSPF dynamic routing

### 3. Server Layer

* Three web servers
* Dedicated server routers
* Server switches

---

## Topology Used

### LAN

* Star Topology

### WAN / Core Network

* Partial Mesh Topology

This combination provides both scalability and fault tolerance.

---

## Key Features

### Dynamic Routing

* OSPF (Open Shortest Path First)
* Automatic route learning
* Fast convergence during failures

### Load Balancing

* Equal-Cost Multi-Path (ECMP)
* Traffic distribution across multiple available routes

### Failover Support

* Automatic traffic rerouting
* Minimal downtime
* Self-healing network behavior

### Redundancy

* Multiple paths to every server
* Elimination of critical single points of failure

---

## Technologies Used

### Simulation Software

* Cisco Packet Tracer 8.x

### Networking Protocols

* OSPF
* TCP
* HTTP
* FTP
* DNS

### Network Services

* DHCP
* DNS
* HTTP Web Services

---

## Network Devices

| Device              | Purpose          |
| ------------------- | ---------------- |
| Cisco 2911 Routers  | Routing and OSPF |
| Cisco 2960 Switches | LAN connectivity |
| Web Servers         | HTTP services    |
| DNS Server          | Name resolution  |
| PCs                 | Client systems   |
| Printer             | Network resource |

---

## IP Addressing Scheme

### Client Network

| Network      | CIDR |
| ------------ | ---- |
| 192.168.10.0 | /24  |

### Server Networks

| Network     | CIDR |
| ----------- | ---- |
| 172.16.10.0 | /24  |
| 172.16.20.0 | /24  |
| 172.16.30.0 | /24  |

### Router Links

* Multiple /30 subnets were used for point-to-point router connections to optimize IP utilization.

---

## Implementation Steps

1. Create the network topology in Cisco Packet Tracer.
2. Configure IP addressing on all devices.
3. Configure DHCP services.
4. Configure OSPF on all routers.
5. Configure HTTP and DNS services.
6. Verify OSPF neighbor relationships.
7. Test connectivity using Ping and Traceroute.
8. Simulate failures and verify failover functionality.

---

## Testing Performed

### Connectivity Testing

* Ping between clients and servers
* End-to-end reachability verification

### Path Verification

* Traceroute analysis
* Route validation

### Failure Testing

* Link failures
* Route failures
* OSPF reconvergence testing

### Performance Analysis

* Throughput observation
* Delay measurement
* Packet loss monitoring

---

## Results

The simulation successfully demonstrated:

* Continuous web service availability
* Automatic failover during link failures
* Dynamic route recalculation using OSPF
* Traffic distribution through ECMP
* Minimal packet loss during network disruptions

---

## Advantages

* High Availability
* Automatic Failover
* Load Distribution
* Improved Reliability
* Scalability
* Cost-Effective Implementation
* Simplified Network Management

---

## Limitations

* Dependence on OSPF convergence time
* No dedicated Layer 4/7 load balancer
* Simulation-based environment
* Remaining single points of failure (LAN Router and Internet Router)
* No security mechanisms such as ACLs or Firewalls
* IPv4-only implementation

---

## Future Enhancements

* Multi-Area OSPF Deployment
* BGP Integration
* Dedicated Load Balancers
* IPv6 Support
* Firewall and ACL Implementation
* VPN Integration
* Network Monitoring Tools
* Automation using Python or Ansible
* Server Clustering and Content Replication

---

## Learning Outcomes

This project provides practical experience in:

* Dynamic Routing Protocols
* OSPF Configuration
* Network Redundancy
* Load Balancing Concepts
* Failover Mechanisms
* IP Addressing and Subnetting
* Enterprise Network Design
* Cisco Packet Tracer Simulation

---

## Authors

Developed as a Data Communication course project to demonstrate High Availability networking concepts using Cisco Packet Tracer.

---

## License

This project is intended for academic and educational purposes.

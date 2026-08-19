# CapeTech Solutions — Small Business Network Infrastructure

## Project Overview

This project simulates a small business network for **CapeTech Solutions**, an IT company with 10 employees across three departments:

* **IT:** 3 employees
* **HR:** 3 employees
* **Finance:** 4 employees

The network was designed and implemented using **Cisco Packet Tracer** to provide reliable internal connectivity and centralized network services.

## Objectives

The objectives of this project were to:

* Design a small-business network topology
* Configure a Cisco router and switches
* Implement IPv4 addressing
* Configure DHCP for automatic IP assignment
* Configure a central DNS server
* Configure switch management addresses
* Implement basic device access security
* Test connectivity between network devices and end-user devices

## Network Topology

The network consists of:

* 1 × Cisco 2911 Router
* 2 × Cisco 2960 Switches
* 10 × Employee PCs
* 1 × Server

### Department Distribution

| Department | Employees |    Devices |
| ---------- | --------: | ---------: |
| IT         |         3 |      3 PCs |
| HR         |         3 |      3 PCs |
| Finance    |         4 |      4 PCs |
| **Total**  |    **10** | **10 PCs** |

## IP Addressing Plan

| Device       | IP Address     | Assignment |
| ------------ | -------------- | ---------- |
| CPT-R1       | 192.168.10.1   | Static     |
| CPT-SW1      | 192.168.10.2   | Static     |
| CPT-SW2      | 192.168.10.3   | Static     |
| CPT-SERVER01 | 192.168.10.10  | Static     |
| Employee PCs | 192.168.10.21+ | DHCP       |

**Network:** `192.168.10.0/24`

**Subnet Mask:** `255.255.255.0`

**Default Gateway:** `192.168.10.1`

## Technologies and Services

* Cisco Packet Tracer
* Cisco IOS
* IPv4
* DHCP
* DNS
* Ethernet switching
* Basic router configuration
* Basic switch configuration
* Network connectivity testing

## Configuration Highlights

### Router

The router was configured as the default gateway using:

`192.168.10.1`

The router also provides DHCP services to employee PCs.

### DHCP

The DHCP pool automatically assigns IP addresses to employee devices.

Infrastructure addresses from:

`192.168.10.1 – 192.168.10.20`

were excluded from the DHCP pool.

### DNS

A central DNS service was configured on:

`192.168.10.10`

The following internal DNS record was created:

`server.capetech.local → 192.168.10.10`

### Switch Management

The switches were assigned management addresses:

* CPT-SW1 — `192.168.10.2`
* CPT-SW2 — `192.168.10.3`

## Network Testing

The completed network was tested using:

### Router Connectivity

Employee PCs were tested against the default gateway:

`ping 192.168.10.1`

### Server Connectivity

Employee PCs were tested against the central server:

`ping 192.168.10.10`

### DNS Resolution

The DNS configuration was tested using:

`ping server.capetech.local`

### DHCP Verification

DHCP leases were verified on the router using:

`show ip dhcp binding`

### Interface Verification

Router interface status was verified using:

`show ip interface brief`

## Project Screenshots

### Network Topology

![Network Topology](screenshots/01-network-topology.png)

### DHCP Bindings

![DHCP Bindings](screenshots/02-dhcp-bindings.png)

### Router Interface Status

![Router Interface Status](screenshots/03-router-interface-status.png)

### PC DHCP Configuration

![PC DHCP Configuration](screenshots/04-pc-dhcp-configuration.png)

### PC to Router Connectivity

![PC to Router Ping](screenshots/05-pc-to-router-ping.png)

### PC to Server Connectivity

![PC to Server Ping](screenshots/06-pc-to-server-ping.png)

### DNS Test

![DNS Test](screenshots/07-dns-test.png)

## Skills Demonstrated

Through this project, I demonstrated practical experience with:

* Network topology design
* IPv4 addressing
* DHCP configuration
* DNS configuration
* Cisco router configuration
* Cisco switch configuration
* Network troubleshooting
* Connectivity testing
* Basic network security
* Technical documentation

## Future Improvements

This network provides a foundation for more advanced security improvements.

Future versions could include:

* VLAN segmentation
* Inter-VLAN routing
* Access Control Lists (ACLs)
* SSH-based device management
* Port security
* Network hardening
* Security monitoring

## Project Files

* `CapeTech-Small-Business-Network.pkt` — Cisco Packet Tracer project
* `screenshots/` — Project configuration and testing evidence
* `README.md` — Project documentation

---

**Project:** CapeTech Solutions Small Business Network
**Platform:** Cisco Packet Tracer


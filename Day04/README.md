```markdown
# Networking & Cybersecurity Fundamentals 🛡️

This document provides concise, cybersecurity-focused definitions for fundamental networking concepts.

---

## TCP vs. UTP

This is a common point of confusion. These two terms describe different things at different network layers and have distinct security implications.

* **TCP (Transmission Control Protocol):** A Layer 4 (Transport) protocol that ensures reliable data delivery. From a security perspective, TCP is a frequent target of attacks like **TCP SYN Floods** (a type of Denial of Service attack) and **TCP Session Hijacking**, where an attacker takes over a valid communication session.

* **UTP (Unshielded Twisted Pair):** A type of Layer 1 (Physical) network cable. Its primary security vulnerability is physical. An attacker with physical access can use a **network tap** on a UTP cable to eavesdrop on (sniff) unencrypted network traffic or inject malicious packets.

---

## Network

In cybersecurity, a **network** is the primary battleground. It's the entire system of interconnected devices (computers, servers, IoT devices) that an organization must defend. Every connection point is a potential entry point for an attacker, and the entire network infrastructure must be monitored for malicious activity, fortified against intrusion, and designed to be resilient.

---

## Subnet

A **subnet** (or subnetwork) is a crucial defensive tool used for **network segmentation**. By dividing a large network into smaller, isolated subnets, security teams can contain breaches. If an attacker compromises one subnet, segmentation acts as a barrier, preventing them from moving laterally to access other critical parts of the network. This strategy allows for more granular security policies and monitoring.

---

## MAC Address

A **MAC (Media Access Control) address** is a unique, hard-coded hardware identifier for a device's network interface.

* **Defense:** Security teams use MAC addresses for **MAC filtering**, a security measure that only allows pre-approved devices to connect to a network.
* **Attack:** Attackers can perform **MAC spoofing**, where they alter their device's MAC address to impersonate a trusted device, thereby bypassing MAC filtering controls.

---

## IP Address

An **IP (Internet Protocol) address** is a logical address assigned to a device on a network. It's essential for identifying and locating devices for communication. In cybersecurity, IP addresses are critical for:

* **Threat Intelligence:** Identifying the source of an attack by tracing malicious activity back to a specific IP.
* **Blocking:** Configuring firewalls and intrusion prevention systems to block traffic from known malicious IP addresses.
* **Geolocation:** Determining the approximate geographic location of a device, which can help in attributing attacks.

---

## IPv6 vs. IPv4 (Static & Dynamic)

### IPv4 vs. IPv6

* **IPv4 (Internet Protocol v4):** The older standard with a limited (~4.3 billion) 32-bit address space.
* **IPv6 (Internet Protocol v6):** The new standard with a virtually limitless 128-bit address space. From a security perspective, IPv6 was designed with improvements, most notably the mandatory integration of **IPsec**, which provides authentication and encryption at the IP packet level. However, misconfigured or poorly managed dual-stack (IPv4 and IPv6) environments can introduce new, overlooked vulnerabilities.

### Static vs. Dynamic IP Addresses

* **Static IP:** A fixed IP address that does not change. While easier to manage for firewall rules, a static IP provides a constant, predictable target for attackers.
* **Dynamic IP:** A temporary IP address assigned from a pool by a DHCP server. For an attacker, a dynamic IP can make it slightly harder to target a specific end-user device over time. For defenders, it makes diligent log-keeping essential to correlate an IP address with a specific user at the time of an incident.

```

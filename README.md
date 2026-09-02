# Linux Server Administration & Failure Recovery Lab

> **Ubuntu Server | Bash | SSH | systemd | Virtualization**

A hands-on Linux infrastructure laboratory focused on deploying, administering, monitoring, troubleshooting, and recovering Linux server environments.

This project simulates a small multi-node server infrastructure where Linux systems are configured, accessed remotely, monitored, deliberately exposed to controlled failures, diagnosed, recovered, and documented.

The primary goal is to develop practical Linux system administration and infrastructure troubleshooting skills through repeatable hands-on experiments.

---

## Table of Contents

- [Overview](#overview)
- [Objectives](#objectives)
- [Technology Stack](#technology-stack)
- [Lab Architecture](#lab-architecture)
- [Environment Setup](#environment-setup)
- [Server Deployment](#server-deployment)
- [User and Group Management](#user-and-group-management)
- [File Permissions](#file-permissions)
- [Package Management](#package-management)
- [SSH Remote Administration](#ssh-remote-administration)
- [Static Network Configuration](#static-network-configuration)
- [systemd and Service Management](#systemd-and-service-management)
- [System Monitoring](#system-monitoring)
- [Log Analysis](#log-analysis)
- [Failure Injection and Recovery](#failure-injection-and-recovery)
- [Troubleshooting Methodology](#troubleshooting-methodology)
- [Bash Automation](#bash-automation)
- [Testing and Validation](#testing-and-validation)
- [Repository Structure](#repository-structure)
- [Results](#results)
- [Key Skills Demonstrated](#key-skills-demonstrated)
- [Future Improvements](#future-improvements)
- [Safety](#safety)
- [Author](#author)

---

# Overview

This project is designed as a practical Linux infrastructure lab rather than a collection of isolated Linux command exercises.

The environment contains multiple Ubuntu Server nodes running inside a virtualized network.

The systems are used to practice:

- Linux server deployment
- System administration
- User and group management
- File permissions
- Package management
- SSH-based remote administration
- Static network configuration
- Service management
- System monitoring
- Log analysis
- Failure diagnosis
- Root-cause analysis
- Recovery procedures
- Bash automation

A major component of the project is **controlled failure injection**.

Instead of only building systems that work, the lab intentionally introduces common infrastructure failures and uses a structured troubleshooting process to identify and resolve them.

---

# Objectives

The main objectives of this project are:

1. Deploy multiple Ubuntu Server systems in a virtualized environment.
2. Configure and administer Linux systems from the command line.
3. Manage users, groups, permissions, and ownership.
4. Configure SSH for remote administration.
5. Configure static IPv4 networking.
6. Understand Linux services and `systemd`.
7. Monitor CPU, memory, disk, processes, and services.
8. Analyze system and service logs.
9. Troubleshoot DNS and networking failures.
10. Diagnose permission and service failures.
11. Investigate storage and resource exhaustion.
12. Automate repetitive administrative and diagnostic tasks using Bash.
13. Develop a repeatable infrastructure troubleshooting methodology.
14. Document every failure, diagnosis, resolution, and verification step.

---

# Technology Stack

| Category | Technology |
|---|---|
| Operating System | Ubuntu Server |
| Virtualization | VirtualBox / VMware |
| Shell | Bash |
| Remote Administration | OpenSSH |
| Service Management | systemd |
| Networking | TCP/IP, IPv4 |
| Network Diagnostics | ip, ping, traceroute, ss, dig, nslookup |
| Monitoring | top, htop, ps, free, df, uptime |
| Logs | journalctl |
| Automation | Bash |
| Version Control | Git |
| Repository | GitHub |

---

# Lab Architecture

The lab uses multiple Ubuntu Server virtual machines connected through an isolated virtual network.

A basic architecture is:

```text
                         Host Machine
                              |
                       Virtualization
                              |
                    Isolated Lab Network
                              |
              +---------------+---------------+
              |                               |
              v                               v
       +-------------+                 +-------------+
       | Ubuntu      |                 | Ubuntu      |
       | Server 01   |                 | Server 02   |
       |             |                 |             |
       | Admin Node  |                 | Service Node|
       +-------------+                 +-------------+
              |                               |
              +---------------+---------------+
                              |
                       SSH / TCP-IP

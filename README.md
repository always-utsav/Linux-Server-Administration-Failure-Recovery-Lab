# Linux Server Administration & Failure Recovery Lab

Hands-on Linux infrastructure lab focused on Ubuntu Server deployment, system administration, networking, service management, monitoring, and troubleshooting.

## Overview

This project simulates a small Linux server environment used to practice real-world infrastructure administration and failure recovery.

The lab covers server configuration, remote administration, system monitoring, controlled failure injection, root-cause analysis, and recovery.

## Tech Stack

- Ubuntu Server
- Bash / Linux CLI
- SSH
- systemd
- VirtualBox
- Git & GitHub

## Key Areas

- Ubuntu Server installation and configuration
- User, group, and permission management
- Package and service management
- SSH-based remote administration
- Static IP and network configuration
- Process, CPU, memory, and disk monitoring
- Linux logs and system diagnostics
- Network troubleshooting
- Bash automation
- Failure injection and recovery

## Failure Scenarios

The lab includes controlled failures such as:

- DNS configuration issues
- SSH and service failures
- Incorrect file permissions
- Network misconfiguration
- Disk space exhaustion
- High CPU or memory usage
- Failed systemd services

Each failure is investigated using a structured workflow:

**Observe → Diagnose → Identify Root Cause → Recover → Verify**

## Monitoring & Diagnostics

System health is monitored using standard Linux utilities and custom Bash scripts.

Monitored areas include:

- CPU and memory utilization
- Disk usage
- Running processes
- Service status
- Network connectivity
- DNS resolution
- System logs

## Automation

Bash scripts are used to automate:

- System health checks
- Resource monitoring
- Service status checks
- Network diagnostics
- Basic troubleshooting reports

## Repository Structure

```text
linux-infrastructure-lab/
├── scripts/
│   ├── health-check.sh
│   ├── resource-monitor.sh
│   └── network-diagnostics.sh
├── configs/
├── troubleshooting/
├── documentation/
└── README.md

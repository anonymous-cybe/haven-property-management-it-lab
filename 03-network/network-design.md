# Haven Property Management - Network Design

# Purpose

This document describes the network architecture for the simulated
Haven Property Management Ltd IT environment.

# Lab Network

Network: 192.168.50.0/24

The initial lab environment will use an isolated Hyper-V
internal virtual switch.

# Devices

| Device | Role | IP Address |
|---|---|---|
| HAVEN-DC01 | Windows Server / Domain Controller | 192.168.50.10 |
| HAVEN-PC01 | Windows 11 Employee Workstation | 192.168.50.20 |

## Network Architecture

```text
HAVEN-LAB
192.168.50.0/24
       |
       +----------------+
       |                |
       v                v
 HAVEN-DC01         HAVEN-PC01
 .10                .20
 Windows Server     Windows 11
```

## Virtual Network Implementation

### Hyper-V Virtual Switch

Name: HAVEN-LAB

Type: Internal

Purpose:

The HAVEN-LAB virtual switch provides an isolated virtual network
for the simulated Haven Property Management environment.

The Internal switch allows the virtual machines to communicate
with each other and allows the physical Windows host to participate
in the laboratory network.

Internet access is intentionally not provided at this stage.
Internet connectivity will be introduced later when required by
specific lab exercises.

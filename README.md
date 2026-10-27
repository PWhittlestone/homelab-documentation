# homelab-documentation
My personal Homelab setup currently and future plans for expansion
# My Homelab: Networking and Self-Hosted Infrastructure

## Overview

I built my homelab to develop practical skills in networking, Linux administration, server management, virtualization, containerization, and infrastructure troubleshooting. My environment combines a TrueNAS SCALE server, a Raspberry Pi, and an Ubuntu workstation to host services, manage network resources, and experiment with self-hosted applications.

My goal is to understand how the systems behind modern networks operate and to develop my skills through hands-on projects, troubleshooting, and continuous improvement.

## Network Infrastructure

My home network uses an ASUS RT-AX89X router as its central networking device. My main systems include:

- **TrueNAS SCALE server:** Hosts self-hosted applications, storage, and game servers.
- **Raspberry Pi 4:** Runs Debian 13, Docker, and AdGuard Home for network-wide DNS filtering.
- **Ubuntu laptop:** My primary workstation for administration, development, remote management, and local AI experimentation.
- **Tailscale:** Connects my major devices to provide secure remote access.

I use SSH keys to simplify remote administration between my Linux systems.

## Self-Hosted Services

My TrueNAS server hosts several applications and services:

| Service | Purpose |
|---|---|
| Jellyfin | Self-hosted media streaming |
| Dispatcharr | Additional media management |
| Immich | Self-hosted photo and video management |
| Scrutiny | Storage drive health monitoring |
| Minecraft Bedrock Server | Multiplayer game hosting |
| Palworld Server | Multiplayer game hosting |
| MeTube | Media downloading |
| File Browser | Browser-based file management |
| Nextcloud | Personal cloud services |
| Collabora | Online document editing integrated with Nextcloud |

I organize storage into separate pools: `nvmepool` for application data and `tank` for larger storage needs.

Many of my applications run in containers, giving me hands-on experience with application configuration, storage mounts, permissions, networking, and troubleshooting.

## DNS and Remote Access

My Raspberry Pi runs AdGuard Home to provide DNS filtering for my home network. This gives me practical experience with DNS services and the role name resolution plays in network connectivity.

Tailscale provides remote connectivity between my TrueNAS server, Raspberry Pi, Ubuntu laptop, and other supported devices. SSH keys allow me to administer Linux systems remotely.

I want to continue developing my understanding of routing, DNS, firewalls, access controls, and network segmentation.

## Projects and Troubleshooting

Maintaining my homelab involves investigating application failures, configuring containers, managing storage permissions, and diagnosing connectivity problems.

Some of my ongoing projects include:

- Improving the reliability of self-hosted applications.
- Managing storage and application data across separate pools.
- Configuring secure remote administration.
- Monitoring drive health and server performance.
- Planning a structured Ethernet installation throughout my home.

I document what I learn as I troubleshoot and improve my infrastructure.

## Future Networking Goals

My next major project is expanding wired Ethernet throughout my single-story home. I am planning approximately 12–20 network drops connected to a centralized location.

This project will help me develop practical skills in:

- Structured Ethernet cabling and cable management.
- Patch panels and network switches.
- TCP/IP and subnetting.
- DNS and DHCP.
- VLANs and network segmentation.
- Firewall configuration and access control.
- Network monitoring and troubleshooting.
- Network diagrams and infrastructure documentation.

I want to build a more reliable, maintainable network while developing the knowledge needed to design and troubleshoot increasingly complex environments.

## Learning Philosophy

I learn best by building real systems, investigating problems, and applying what I discover. My homelab provides an environment where I can experiment, make improvements, and gain practical experience with the technologies used in modern IT infrastructure.

I plan to continue documenting my projects and expanding my networking knowledge through hands-on experimentation and structured learning.
## Network Diagram

```text
                    INTERNET
                       |
                 ASUS RT-AX89X
                       |
                 Home Network
                 /     |      \
                /      |       \
         TrueNAS     Raspberry   Ubuntu
          Server        Pi       Laptop
             |           |          |
       Hosted Apps    AdGuard     Admin and
       and Storage    Home DNS    Development

         Tailscale provides remote connectivity
                between supported devices
```

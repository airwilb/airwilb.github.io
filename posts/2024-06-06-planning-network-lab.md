---
layout: post
title: "Planning My pfSense Network Lab"
date: 2024-06-06
---

# Planning My pfSense Network Lab

## Why I'm Building This
My goal is to transition into a cybersecurity career and while I have dedicated a majority of my time to learning about various attack vectors, vulnerabilities and pentesting tools I have neglected to fully understand the complexities of networking. My goal with this home lab is to explore all the nuances of networking that I believe are an integral and often overlooked part of cybersecurity.

## Current Setup
- Proxmox server running media stack LXC containers (Jellyfin, Jellyseerr, *Arr services) 
- Everything is currently on single network connected directly to my router (vmbr0)
- No segmentation or security considerations as I wanted the media server to be simple and accessible by multiple clients in the home network 

## Goals for This Lab
1. Learn pfSense configuration
2. Create segmented networks with VLANs
3. Build vulnerable AD environment
4. Practice pentesting in isolated environment

## Planned Network Design

Home Router (192.168.1.0/24)
    │
    ├── Existing Proxmox (Media Stack) - UNTOUCHED
    │
    └── New Proxmox Instance/VM
            │
            └── pfSense Firewall (Virtual Router)
                    │
                    ├── Management Network (VLAN 10)
                    ├── Vulnerable AD Network (VLAN 20)
                    ├── Pentesting Network (VLAN 30)
                    └── DMZ Network (VLAN 40)

## Next Steps
- Download and install pfSense
- Create basic two-network setup
- Document the process

*This is a dynamic document - I'll update as I build.*

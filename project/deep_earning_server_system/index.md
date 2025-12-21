---
title: Deep Learning Server System

# Summary for listings and search engines
summary: A deep learning system for small research teams, with multiple GPU servers, centralized network storage, server and user management, 10 GbE network, and per-server SSD cache.

tags:
- Deep Learning

# Date published
date: "2019-10-21T00:00:00Z"

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: false

# Optional external URL for project (replaces project detail page).
external_link: ""

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.
image:
  caption: Completed hardware
  focal_point: Smart
  preview_only: false

# links:
# - icon: twitter
#   icon_pack: fab
#   name: Follow
#   url: https://twitter.com/georgecushen

links:
- name: Docs
  url: 'https://github.com/chengzhag/nas_directory'
url_code: ""
url_pdf: ""
url_slides: ""
url_video: ""

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ""
---

---
## Introduction

For a small research team with more than a dozen of students, several servers with 4 or 8 GPUs are necessary. However, with independent storage for each servers, datasets, codes, and environments are often duplicated across different servers, which is inefficient and troublesome when using different servers. Also, user management becomes a problem if every user needs to be setup on each of the server.

To solve the above problems, a system is built with centralized network storage, server and user management, 10 GbE network, and per-server SSD cache. This can be used as a reference for small academic teams on deep learning or maybe small companies.

For new users and admins, [documentation](https://github.com/chengzhag/nas_directory) (in Chinese) are wrote to provide basic informations and regulations.

## Hardware

### Servers and Network

Our team has 5 existing servers, each with 4 x 1080Ti and a system SSD. The problem is that every server is not able to install an extra 10 GbE Network Interface Card (NIC) since all PCIE ports are preserved for GPUs. Thus an NBASE-T switch is used to connect each server via 5 GbE USB NICs. (A more stable and affordable configuration might be using 10 GbE SFP+ switch with PCIE NIC.)

{{< figure src="照片 012.jpg" caption="No space to install 10 GbE NIC for existing server" width="30%" >}}

### Storage

We chose to use QNAP Network Attached Storage (NAS) TS-932X, which can accommodate 5 x 3.5-inch hard drives and 4 x 2.5-inch SSDs, and has dual 10GbE SFP+ ports. The performance of its ARM processor is quit as SSD cache is configured on each server, which makes it possible to load frequently used data from NAS at the first time.

{{< figure src="IMG_20191107_161030.jpg" caption="NAS and switch" width="30%" >}}

## Software

### NAS

We configure our NAS with a ```Public``` folder (contraining the git repo of [documentation](https://github.com/chengzhag/nas_directory)) for [shared datasets](https://github.com/chengzhag/nas_directory/tree/master/datasets) storage, and a home folder for each user, allowing users to access their environment (e.g. anaconda), codes, and datasets on every server. QNAP NAS provides an easy-to-use operating system with serveral customizable services. In our cases, it is configured with the following services:

- NFS server: For mounting storage on server
- samba server: For mounting storage on client computers
- LDAP server: Centralized authorization and user management for both NAS and GPU server
- Other services like Download Station, file management from browser, restoring from snapshot/recycle bin, Qsync, VPN, DDNS, and iperf3 are also available to users.

### Server

Each server is installed with same version of Ubuntu and Nvidia GPU driver, and is configured with the following services:

- autofs: Automatically mount two types of folders (i.e. user home folders to ```/home``` and ```Public``` folder to ```/media```) through NFS
- cachefilesd: Local SSD cache for NFS
- LDAP authentication: Configured with Pluggable Authentication Modules (PAM)
- ThinLinc: Remote desktop

With the configurations above, students can use the same username to login to NAS or any server, access their data or share datasets with others, and configure anaconda environments once to use them on all servers. A [shell script](https://github.com/chengzhag/nas_directory/blob/master/documents/server/initserver.sh) is used to configure servers. It is validated on Ubuntu 18 and might be used as a reference. For easier deployment and management of servers, virtual machine system (e.g. Proxmox) is installed on each server, with GPU passthrough configured. The difference between virtual machine and bare-metal Ubuntu is barely sensible.

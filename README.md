# My Cybersecurity Homelab Project

This repository documents the setup and experiments conducted in my personal cybersecurity homelab built using VirtualBox on macOS (16GB RAM).

**Goal:** To gain hands-on experience with cybersecurity tools, concepts, and techniques learned through CompTIA Security+, Google Cybersecurity Certificate, and self-study.

---

## Phase 1: Downloads Complete

The following source files have been downloaded into the `Homelab-ISOs` directory:
* Kali Linux Installer ISO
* Metasploitable 2 VM ZIP Archive
* Ubuntu Server LTS ISO
* Windows Server Evaluation ISO
* pfSense CE ISO Installer
* Security Onion ISO

---

## Phase 2: VM Setup Progress

* Successfully imported Metasploitable 2 VM (`Metasploitable2-Linux`) into VirtualBox from the unzipped archive.
* Configured Metasploitable 2 network adapter (Adapter 1) to 'Host-only Adapter' (`vboxnet0`) for network isolation.
* *Next steps: Install Kali Linux VM...*
Re-downloading Metasploitable 2 ZIP archive to find correct OVF file for import.

* (2025-04-28): Created Kali Linux VM profile in UTM (using Emulate x86_64) and started the graphical OS installation.


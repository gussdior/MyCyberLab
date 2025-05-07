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
* (2025-04-28): Decided to skip Metasploitable 2 setup for now due to challenges running the required 32-bit x86 VM on Apple Silicon (M1 Pro) host with available tools. Will focus on other VMs and utilize 
online platforms (TryHackMe/CyberDefenders) for specific vulnerability practice initially.
* (2025-04-28): Switched virtualization software to UTM ([https://mac.getutm.app/](https://mac.getutm.app/)) for better x86_64 emulation capabilities on the host.
* (2025-04-28): Created Kali Linux VM profile in UTM (`Kali Linux (x86_64)`):
    * Set Mode: Emulate, Architecture: x86_64
    * Configured Resources: 4096 MiB RAM, 2 CPU Cores, 64 GiB Disk.
    * Network: Adapter 1 using default 'Shared Network' (NAT); Adapter 2 configured in UTM for 'Internal Network' (`lab-lan`).
* (2025-04-28): Successfully completed the Kali Linux graphical installation using the `amd64` ISO. This involved manually clearing disk partitions via the installer after an initial stall. Ejected ISO via 
UTM drive settings post-install.
* (2025-04-28): Successfully booted and logged into the installed Kali Linux (Xfce) desktop environment.
* (2025-04-28): Verified internet connectivity via `eth0` (`ping 8.8.8.8` successful) from Kali terminal. Noted that the second network interface (`eth1` for `lab-lan`) was not automatically configured by the 
OS yet.
* (2025-04-28): Performed initial system update using `sudo apt update` and `sudo apt full-upgrade -y`.
* *Next steps: Configure the `eth1` internal network interface within Kali, then install Ubuntu Server VM.
* (2025-04-30): Began exploring Kali tools; performed initial Nmap IP Protocol scan (`-sO`) against `scanme.nmap.org` and reviewed command help (`--help`, `man`).
* (2025-05-01): Completed foundational Linux/Networking labs on TryHackMe (e.g., Linux Fundamentals Parts 1-3, Networking Basics) to reinforce core concepts.
* (2025-05-02): Completed Windows Fundamentals 1 lab on Tryhackme.

## Phase 3: SOC Simulator – Phishing Simulation
(2025-05-02): Developed and integrated a basic phishing simulation scenario into the SOC lab environment.

Created a mock phishing email targeting a simulated internal user.

Designed detection logic to trigger alerts on suspicious user behavior (e.g., clicking malicious links).

Simulated credential harvesting through a fake login page hosted on a local web server.

Manually reviewed logs and system behavior to verify phishing indicators (e.g., HTTP requests, user-agent strings).

Documented steps for analyst response workflow in README.

Next steps: Expand phishing scenarios with attachment-based lures and integrate with SIEM for automated alerting.

* (2025-05-03): Successfully installed Kali Linux (x86_64) in UTM using Emulation after troubleshooting boot issues in VirtualBox. Ejected ISO post-install and logged into Kali desktop. Verified internet 
connectivity (`ping`) and performed full system update (`apt update && apt full-upgrade`). Practiced initial Nmap scans (`-sO`, `-sS`, `-sV`) against `scanme.nmap.org`. Configured global Git user name and 
email.

(2025-05-04): Successfully finished Windows Fundamentals 2 on TryHackMe to deepend my understanding with Windows System tools. 

(2025-05-05): Starting SOC Level 1 Course on TryHackMe - Covering day to day Security Analyst tasks.

* Deep coverage of Pyramid of Pain. Going over the things I learned throughout my study journey. 


* (2025-05-06): Cyber Kill Chain framework workshop is finished. 

* (2025-05-07): OverTheWire exercise, reached level 17! Practicing Linux skills.


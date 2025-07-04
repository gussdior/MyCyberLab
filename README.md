V# My Cybersecurity Homelab Project

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
vconnectivity (`ping`) and performed full system update (`apt update && apt full-upgrade`). Practiced initial Nmap scans (`-sO`, `-sS`, `-sV`) against `scanme.nmap.org`. Configured global Git user name and 
email.

(2025-05-04): Successfully finished Windows Fundamentals 2 on TryHackMe to deepend my understanding with Windows System tools. 

(2025-05-05): Starting SOC Level 1 Course on TryHackMe - Covering day to day Security Analyst tasks.

* Deep coverage of Pyramid of Pain. Going over the things I learned throughout my study journey. 


* (2025-05-06): Cyber Kill Chain framework workshop is finished. 

* (2025-05-07): OverTheWire exercise, reached level 17! Practicing Linux skills.
* Continuing to build expertise in SOC Level 1 fundamentals, reinforcing existing knowledge and actively strengthening core skills through practical application.
* In the process of creating my own SIEM machine, to practice and understand the mindset of the use of essential tools."In the process of creating my own SIEM machine, to practice and understand the mindset 
of the use of essential tools.

* (2025-05-08): Docs: Unified Kill Chain.
* (2025-05-10) Docs: Taking a course on ethical hacking by Liang Yang Loi to deepen my understanding on how attackers think.)
* (2025-05-11: Docs: Continuing on Soc Level 1 course on TryHackMe.
* (2025-05-12): Commenced the "Intro to Cyber Threat Intel" module on TryHackMe (SOC Level 1 path) to understand CTI fundamentals and its role in security operations.
* (2025-05-12): Progressed in TryHackMe's CTI module, studying key frameworks such as the Cyber Kill Chain and the Diamond Model of Intrusion Analysis.
* (2025-05-13): Explored common Cyber Threat Intelligence tools and platforms within the TryHackMe CTI module, including the concepts behind MISP and using resources like VirusTotal.
* (2025-05-14): Continued TryHackMe SOC Level 1 path, focusing on the "Intro to Cyber Threat Intel" module and learning about YARA rule basics.
* (2025-05-15): Strengthening my knowledge on core security principals such as Active Directory, Azure.)

* (2025-05-16): Continuing on my skill building for a SOC Analyst position. 

* (2025-05-17): Soc Level 1. Snort finished. 
** "Using IDS/IPS with Snort."
** "Snort Challanges, the basics"

* (2025-05-18) Docs: CySa+ practice course and quiz.)
* (2025-05-19) TryHackMe SOC Level 1, continuiation, and CySa+ practice exams.
* (2025-05-21) Continuation on SOC Level 1 and CySa+ practice exams. 
* (2025-05-22) SOC Level 1, and CySa+ besides actively using Kali Linux to understand attackers mindset.
* (2025-05-25) Continuation of studies, ethical hacking practices on the home-lab.
* (2025-05-26) Added Digital Forensics and Incident Response (DFIR) tools and documentation for enhanced cybersecurity incident handling.
* (2025-05-28) Studying further for Cysa+ exam, and finishing the SOC Level 1 on Trhackme.
* (2025-05-30) Practicing Yara, and applying on my home-lab.

* (2025-06-03): Continued TryHackMe SOC Level 1 path, advancing through the "Intro to Cyber Threat Intel" module, focusing on understanding CTI sources and the intelligence lifecycle.
* (2025-06-03): Explored YARA rule fundamentals within the TryHackMe Cyber Threat Intel module, learning about rule structure and basic signature creation for malware identification.
* Make sure it's added
* (2025-06-10): Practiced SIEM fundamentals within the TryHackMe SOC L1 path, running queries and analyzing logs in simulated Splunk environments.

* (2025-06-10): Advanced in the DFIR module of the TryHackMe SOC L1 path, learning to use tools like Volatility for memory analysis and Autopsy for disk forensics.
* (2025-06-11): Solved OverTheWire Bandit level 9, using a command pipeline of 'strings', 'sort', and 'uniq -u' to find the unique password in the binary data file.
* (2025-06-18): Advanced in OverTheWire Bandit challenges, working on level 12 which required multi-stage file decoding using a pipeline of commands like `xxd`, `gunzip`, and `tar`.

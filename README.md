# NETWORKWALKS-B084-2YU-WK1-PM1-CYBERSECURITY-LAB-SETUP
Isolated virtual cybersecurity lab built with VirtualBox and Kali Linux for ethical hacking practice. Networkwalks Internship, Week 1, Project Module 1.

📌 Project Overview

This project is part of Week 1, Project Module 1 of the Cybersecurity & Ethical Hacking Internship at Networkwalks IT Solutions & Training.

I set up a virtual cybersecurity lab using VirtualBox and Kali Linux. The lab gives me a safe, controlled place to practise security tools such as network scanning, reconnaissance and vulnerability assessment, without touching any real systems.

The lab runs on a private virtual network, so more machines can be added later as targets for authorised testing.

🎯 Objectives
Install and configure VirtualBox
Import Kali Linux as a virtual machine
Create a private NAT Network for the lab
Assign a static IP address to the Kali VM
Test network connectivity and DNS resolution
Take a clean VM snapshot for recovery
Document the full process, including problems and fixes

🛡️ Purpose of the Lab

The lab can be used for:

Network reconnaissance
Port scanning
Vulnerability assessment
Packet analysis
Web security testing
Trying out security tools safely

🐞 Problems Encountered & Solutions

Problem 1. Internet Connectivity After Static IP Configuration
After manually configuring the IPv4 settings, Internet connectivity may fail depending on the Kali/NetworkManager configuration.
$sudo nmcli connection modify "Wired connection 1" ipv4.dad-timeout 0

Problem 2. VirtualBox VT-x / Virtualization Error
The VM initially failed to start because hardware virtualization was disabled in the system firmware/BIOS.

The issue was resolved by:

Restarting the computer.
Entering BIOS/UEFI settings.
Enabling Intel VT-x / hardware virtualization.
Saving the configuration.
Restarting the computer.
Starting the Kali VM again.
After enabling virtualization, the VM started successfully.

What I Learned
Through this project, I learned how to create and configure a virtual environment for cybersecurity practice.

The most important concepts I learned include:

1. NAT vs NAT Network
A standard NAT configuration and a NAT Network serve different purposes.

A NAT Network allows multiple VMs connected to the same virtual network to communicate with one another while providing network address translation for external connectivity.

This makes it useful for building a multi-machine cybersecurity laboratory.

2. Virtual Machine Networking
I learned how VirtualBox virtual network adapters connect virtual machines to different types of networks and how network configuration affects communication between machines.

3. Static IP Configuration
I learned how to configure and verify IPv4 addressing, subnet masks, gateways, and DNS settings in Kali Linux.

4. VM Snapshots
I learned that a clean snapshot should be created before performing risky or experimental activities.

This provides a known-good recovery point for future cybersecurity exercises.

5. Documentation
I learned that documenting commands, configuration, screenshots, problems, and solutions is an important part of a professional cybersecurity project.





# CodeAlpha_Network_Intrustion_Detection_System_TASK-3

# Overview  
This repository provides a step-by-step guide for setting up a Network Intrusion Detection System (NIDS) using **Snort**, developed during Task 3 of my cybersecurity internship at CodeAlpha. This guide will help you configure Snort to monitor network traffic and detect potential threats effectively.  

# Requirements  
✔ A virtualized network where all your VMs can communicate  
✔ A Linux distribution (Ubuntu preferred) for setting up Snort  
✔ Root/Administrative privileges  
✔ Metasploitable 2 vulnerable machine for testing: [Download Here](https://sourceforge.net/projects/metasploitable/)  

# Installation & Setup  

# Step 1: Install and Configure Snort  
- **For Ubuntu:** Follow [this guide](https://www.zenarmor.com/docs/linux-tutorials/how-to-install-and-configure-snort-on-ubuntu-linux).  
- **For Kali Linux:** Check out [this tutorial](https://bin3xish477.medium.com/installing-snort-on-kali-linux-9c96f3ab2910).  

# Step 2: Configure Snort Rules  
- Always back up your Snort configuration file before making changes.  
- Write custom detection rules or use Snort’s default ones:  

```bash
vim /etc/snort/rules/local.rules
```

# Step 3: Start Snort & Monitor Traffic  
Run Snort in listening mode on the appropriate network interface:  

```bash
sudo snort -q -l /var/log/snort -i eth0 -A console -c /etc/snort/snort.conf
```
*(Check your interface name with `ifconfig` or `ip a` and replace `eth0` if necessary.)*  

# Step 4: Simulate Attacks & Analyze Alerts  
- Use **Nmap** to scan the Metasploitable 2 machine.  
- Launch attacks using the **Metasploit framework** and observe the alerts triggered in Snort’s logs.  
- If any errors occur, troubleshoot by reviewing logs and adjusting configurations.  

# Resources 
- [Snort Basics & Setup Guide](https://www.youtube.com/watch?v=Gh0sweT-G30)  
- [Intrusion Detection with Snort](https://www.youtube.com/watch?v=r1Z7SxewjhM)  

# Contributing 
If you encounter issues or have suggestions for improving this guide, feel free to open an issue or submit a pull request. Your contributions are always welcome!  

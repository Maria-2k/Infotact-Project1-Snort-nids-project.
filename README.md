# Infotact Cybersecurity Internship - Project 1  
### Title: Network Intrusion Detection Using Snort IDS  

## Project Overview  
This project focuses on implementing and analyzing **Snort**, an open-source Network Intrusion Detection System (NIDS), to detect and analyze network intrusions in real time.  
The project was implemented on **Kali Linux** to understand Snort’s working principles, configure custom rules, and monitor network traffic for malicious patterns.

---

## Objectives  
- Install and configure Snort IDS on Kali Linux.  
- Understand signature-based intrusion detection.  
- Create and test custom Snort rules.  
- Analyze and interpret alerts for benign and malicious traffic.  

---

## Methodology  

### Step 1: Environment Setup  
- Installed and configured **Snort IDS on Kali Linux**.  
- Updated dependencies and configured the network interface in promiscuous mode.  
- Verified installation using:  
  ```
  snort -V
  snort -T -c /etc/snort/snort.conf
  ```

### Step 2: Capturing Benign Traffic  
- Generated normal traffic (web browsing, DNS queries).  
- Verified Snort’s packet-capturing capabilities.  

### Step 3: Creating Custom Rules  
- Created and tested rules to detect ICMP and suspicious port scans.  
  Example:  
  ```
  alert icmp any any -> any any (msg:"ICMP Ping Detected"; sid:1000001; rev:1;)
  ```
- Added rules to `/etc/snort/rules/local.rules` and restarted Snort.  

### Step 4: Generating and Detecting Malicious Traffic  
- Used `nmap` to simulate port scans and observed triggered alerts.  
- Monitored `/var/log/snort/alert` for intrusion logs.  

### Step 5: Documentation  
- Captured screenshots for:
  - Snort installation
  - Rule configuration
  - Alert generation
- Compiled the results into a detailed report (`project-report.pdf`) uploaded in this repository.  

---

## Observations & Results  
- Snort successfully detected and logged malicious activities.  
- Custom rules improved detection specificity.  
- Benign traffic produced no false positives.  

---

## Key Learnings  
- Gained hands-on experience with Snort NIDS configuration and alert analysis.  
- Understood the significance of intrusion detection in SOC environments.  
- Learned how to write and implement Snort rules effectively.  

---

## Repository Contents  
- `project-report.pdf` – Full project report documentation.  
- `screenshots/` – Evidence of setup, rule creation, and detection.  
- `README.md` – Project overview and methodology.  

---

## Author  
**Maria Jose**  
Cybersecurity Intern – Infotact

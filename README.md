 <div align="center">

# Footprinting & Reconnaissance Attacks with Multiple Kali Tools

Performing website footprinting and reconnaissance using multiple Kali Linux tools.

<p align="center">
  <img src="https://img.shields.io/badge/Project-Footprinting%20%26%20Reconnaissance-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Kali%20Linux-v2026.3-E87500?style=flat-square&labelColor=000000&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/Focus-Reconnaissance-C00000?style=flat-square&labelColor=000000" />
  <img src="https://img.shields.io/badge/Tools-6-238F89?style=flat-square&labelColor=000000" />
  <img src="https://img.shields.io/badge/Techniques-Website%20Footprinting-0070C0?style=flat-square&labelColor=000000" />
  <img src="https://img.shields.io/badge/Target-networkwalks.com-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Platform-GitHub-404040?style=flat-square&labelColor=0070C0&logo=github&logoColor=white" />
  <img src="https://img.shields.io/badge/Program-NetworkWalks-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Week-02-0070C0?style=flat-square" />
  <img src="https://img.shields.io/badge/Module-01-C00000?style=flat-square" />
  <img src="https://img.shields.io/badge/Mentor-Waqas%20Karim%20(CCIE)-C00000?style=flat-square" />
</p>

</div>

## Lab Overview

This project focuses on performing website footprinting and reconnaissance using multiple tools available in Kali Linux. It involves gathering publicly available information about `networkwalks.com`, including domain registration details, IP addresses, web technologies, HTTP response headers, firewall information, and DNS records.

The practical exercises demonstrate how reconnaissance tools help identify publicly exposed information and understand a website's infrastructure as part of the initial phase of cybersecurity assessment.
NetworkWalks project focused on website footprinting and reconnaissance using multiple Kali Linux tools.

## 🎯 Lab Objectives

- Perform domain footprinting using WHOIS to identify registration information.
- Identify website technologies using WhatWeb.
- Resolve domain names to IP addresses using NSLookup.
- Analyze HTTP response headers using cURL.
- Detect Web Application Firewall (WAF) protection using WAFW00F.
- Enumerate DNS records using DNSRecon.
- Understand how reconnaissance helps identify publicly exposed information about a website.

## 🛡️ Lab Purpose and Security Scope

This lab provides a practical environment for learning website footprinting and reconnaissance using multiple Kali Linux tools. It focuses on gathering and analyzing publicly available information about `networkwalks.com` to understand its domain registration, IP addressing, web technologies, HTTP headers, firewall protection, and DNS infrastructure.

The lab covers the following activities:

- Domain registration information gathering.
- Website technology fingerprinting.
- Domain and IP address resolution.
- HTTP response header analysis.
- Web Application Firewall detection.
- DNS record enumeration.

**Security Notice:** All activities must be conducted within the scope of the assigned project and in accordance with applicable authorization. Information gathering should be limited to the specified target and permitted techniques. Do not attempt unauthorized access, exploitation, or testing of systems outside the approved scope.

## ⚙️ Cybersecurity Lab System Specifications

| Component | Specifications |
|---|---|
| Host Operating System | Kali Linux 2026.3 |
| Virtualization Platform | Oracle VirtualBox 7.2.20 |
| Virtual Machine | Kali Linux 2026.3 |
| Network Environment | Existing Cybersecurity Lab |
| Target Domain | networkwalks.com |
| Reconnaissance Tools | WHOIS, WhatWeb, NSLookup, cURL, WAFW00F, DNSRecon |

## ⚙️ Cybersecurity Lab Setup Steps

## Step 1: Initialize the Kali Linux Virtual Machine

Start the Kali Linux 2026.3 VM in VirtualBox, log in, and verify that the desktop loads successfully.

<img width="1319" height="767" alt="kali initalization" src="https://github.com/user-attachments/assets/211bc0e6-fc2f-4d89-8a17-e294a845b566" />


## Step 2: Launch the Kali Linux Terminal

Launch the terminal from the Kali Linux desktop and verify that the command prompt is ready.

<img width="1319" height="767" alt="Kali terminal" src="https://github.com/user-attachments/assets/598e3004-2199-46e7-9139-cdfce4f2347a" />


## Step 3: WHOIS – Domain Registration Lookup

WHOIS is a command-line tool used to retrieve publicly available domain registration information, including registrar details, registration dates, and name servers.

**Command:**

```bash
whois networkwalks.com
```

<img width="1330" height="791" alt="whois" src="https://github.com/user-attachments/assets/f3dff2b5-3570-4373-b82d-55c08350ed8b" />


## Step 4: WhatWeb – Website Technology Fingerprinting

WhatWeb is a Kali Linux reconnaissance tool used to identify technologies running on a website, including web servers, content management systems (CMS), frameworks, and plugins.

**Command:**

```bash
whatweb networkwalks.com
```
<img width="1319" height="767" alt="whatweb" src="https://github.com/user-attachments/assets/1dc5f65b-f455-464d-a849-6908a4caefdf" />


## Step 5: NSLookup – Domain Name Resolution

NSLookup is a command-line tool used to query DNS servers and retrieve domain information, including corresponding IP addresses.

**Command:**

```bash
nslookup networkwalks.com
```

<img width="1319" height="767" alt="nslookup" src="https://github.com/user-attachments/assets/07bda450-75b4-4b07-b0ce-5ffd595d1737" />


### Step 6: cURL – HTTP Response Header Analysis

cURL is a command-line tool used to retrieve HTTP response headers from a website, revealing information such as server details, response status, cookies, and redirects.

**Command:**

```bash
curl -I https://networkwalks.com
```

<img width="1319" height="767" alt="curl -i" src="https://github.com/user-attachments/assets/6fb29e1f-91cc-47cf-a1dd-10c3088ef966" />


## Step 7: WAFW00F – Web Application Firewall Detection

WAFW00F is a Kali Linux reconnaissance tool used to identify whether a website is protected by a Web Application Firewall (WAF) and detect its type.

**Command:**

```bash
wafw00f https://networkwalks.com
```

<img width="1319" height="767" alt="wafw00f" src="https://github.com/user-attachments/assets/68483a6d-fea2-4992-b120-2065bdab4e2f" />


## Step 8: DNSRecon – DNS Record Enumeration

DNSRecon is a Kali Linux reconnaissance tool used to enumerate DNS records and gather information about a domain's DNS infrastructure, including name servers, mail servers, and TXT records.

**Command:**

```bash
dnsrecon -d networkwalks.com
```


# 🐞 Problems Encountered & Solutions

Documenting troubleshooting steps helps improve the lab setup and provides a useful reference for future troubleshooting.

## Problem 1: DNSRecon Timeout Error

While performing DNS enumeration, DNSRecon returned a timeout error because the DNS server did not respond within the default 3-second timeout.

**Solution:** Increased the DNS query timeout to 10 seconds using the `--lifetime` option, allowing more time for the DNS server to respond.

**Command:**

```bash
dnsrecon -d networkwalks.com --lifetime 10
```


# 💡 What I Learned

Through this project, I gained practical experience in website footprinting and reconnaissance using multiple tools available in Kali Linux.

The most important concepts I learned include:

### 1. Domain Registration Information

I learned how to use WHOIS to retrieve publicly available domain registration details, including registrar information, registration dates, and name servers.

### 2. Website Technology Fingerprinting

I learned how to use WhatWeb to identify technologies running on a website, including web servers, content management systems (CMS), frameworks, and plugins.

### 3. DNS Resolution

I learned how to use NSLookup to query DNS servers and resolve domain names into their corresponding IP addresses.

### 4. HTTP Response Header Analysis

I learned how to use cURL to retrieve and analyze HTTP response headers, including server information, response status, cookies, and redirects.

### 5. Web Application Firewall Detection

I gained experience using WAFW00F to identify whether a website is protected by a Web Application Firewall (WAF).

### 6. DNS Record Enumeration

I learned how to use DNSRecon to enumerate DNS records, including name servers, mail servers, SPF, and TXT records.

### 7. Reconnaissance and Information Gathering

I developed a better understanding of how different reconnaissance tools work together to collect publicly available information and build an overview of a website's infrastructure.

---

# 🔐 Security & Ethical Use

This project was conducted for educational purposes as part of the NetworkWalks cybersecurity training program. All reconnaissance activities were limited to the assigned target and authorized scope. Any further security testing must be performed only with explicit permission.

---

# 🔗 Tools & Resources

- **WHOIS:** Domain registration lookup.
- **WhatWeb:** Website technology fingerprinting.
- **NSLookup:** DNS resolution.
- **cURL:** HTTP response header analysis.
- **WAFW00F:** Web Application Firewall detection.
- **DNSRecon:** DNS record enumeration.
- **Kali Linux:** [https://www.kali.org/get-kali/](https://www.kali.org/get-kali/)

---

# 👤 Author

**Amon Alex**  
Cybersecurity Student B084 | Electronics, Telecommunications & Cybersecurity

**LinkedIn:** [Amon Alex](https://www.linkedin.com/in/amon-lowasa-60877a42a/)

## 📌 Project Information

**Program Name:** Cybersecurity at NetworkWalks | **Week:** 02 | **Project:** Footprinting & Reconnaissance Attacks with Multiple Kali Tools | **Repository:** GitHub


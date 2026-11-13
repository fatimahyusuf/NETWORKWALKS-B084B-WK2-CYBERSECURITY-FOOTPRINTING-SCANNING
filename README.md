# NETWORKWALKS-B084B-WK2-CYBERSECURITY-FOOTPRINTING-SCANNING

# Week 2 Project- Footprinting and Network Scanning 

## Project Overview 

This project focused on developing practical cybersecurity skills in footprinting and network scanning using various tools in Kali Linux. It involved using WHOIS, WhatWeb, Nslookup, Curl -I, wafw00f, and DNSRecon to gather information about target domains and identify their infrastructure and security technologies. It also covered footprinting with the Google Hacking Database (GHDB) to discover publicly available information, using theHarvester to collect information such as email addresses and subdomains, and performing network scanning with Zenmap to identify active hosts, open ports, and network services. Overall, the project provided hands-on experience with reconnaissance, information gathering, and network scanning techniques used in the initial stages of ethical hacking and cybersecurity assessments.

# Module 1 (WK1-PM1): Footprinting With Multiple Kali Tools 


## Task 1- Domain Registration Information Gathering Using WHOIS 

### Command 
```txt
whois networkwalks.com
```
### Purpose 
WHOIS is used to gather domain registration details, including the registrar, registration and expiration dates, name servers, and publicly available registrant information.
### Evidence 
<img width="877" height="697" alt="Screenshot 2026-11-09 145508" src="https://github.com/user-attachments/assets/8c8dc160-3ae3-4863-865e-b3d16f4bae73" />
<img width="916" height="748" alt="Screenshot 2026-11-09 145806" src="https://github.com/user-attachments/assets/3d13a835-f9db-4633-9b3b-c46908e4954e" />
<img width="1041" height="775" alt="Screenshot 2026-11-09 145704" src="https://github.com/user-attachments/assets/d601aa28-94a3-4aae-a52f-ee970afa52e6" />

## Task 2- Web Technology Identification Using WhatWeb

### Command
```txt
whatweb networkwalks.com
```
### Purpose 
WhatWeb is used to identify the technologies, frameworks, content management systems, and web servers running on a website.
### Evidence 
<img width="967" height="400" alt="Screenshot 2026-11-09 151504" src="https://github.com/user-attachments/assets/5639e5e3-3f01-4c84-8c84-81cd6e1880cc" />

## Task 3- Domain Name Resolution Using NSLookup

### Command 
```txt
nslookup networkwalks.com
```
### Purpose 
Used to resolve a domain name into its corresponding IP address and retrieve DNS information.
### Evidence 
<img width="601" height="347" alt="Screenshot 2026-11-09 151627" src="https://github.com/user-attachments/assets/41a7fa2c-0045-49f1-a6b4-43f4fb078267" />

## Task 4- HTTP Response Header Analysis Using curl -I 

### Command 
```txt
curl -I https://networkwalks.com
```
### Purpose 
Used to retrieve and examine HTTP response headers from a web server.
### Evidence 
<img width="911" height="489" alt="Screenshot 2026-11-09 151939" src="https://github.com/user-attachments/assets/ef5ec7b9-92f1-4d8e-8fb6-660562a3bbc6" />

## Task 5: Web Application Firewall Detection Using Wafw00f

### Command 
```txt
wafw00f networkwalks.com
```
### Purpose 
Used to identify whether a website is protected by a Web Application Firewall (WAF)
### Evidence
<img width="877" height="440" alt="Screenshot 2026-11-09 152158" src="https://github.com/user-attachments/assets/dfc96f63-b8e8-41b9-96ee-8cbc96c59e70" />

## Task 6: DNS Record Enumeration Using DNSRecon

### Command 
```txt
dnsrecon -d networkwalks.com
```
### Purpose 
Used to enumerate DNS records and gather information about a domain's DNS infrastructure.
### Evidence 
<img width="912" height="634" alt="Screenshot 2026-11-09 152526" src="https://github.com/user-attachments/assets/e3c6b502-e694-4be7-af1b-6a06fd42b393" />


## WK2-PM1- Findings Summary

Here is a more professional and well-structured version for your project documentation:

| Task | Tool Used | Objective                                      | Findings                                                                      |
| -------- | ------------- | -------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| 1        | WHOIS         | Gather domain registration information.            | GoDaddy identified as the registrar, HostGator name servers found, and DNSSEC was unsigned. |
| 2        | WhatWeb       | Identify technologies used by the website.         | Apache, WordPress, WordPress Download Manager, jQuery, and Bootstrap were detected.         |
| 3        | NSLookup      | Resolve the domain name to its IP address.         | `networkwalks.com` resolved to `192.232.216.135`.                                           |
| 4        | cURL          | Examine HTTP response headers.                     | Apache, HTTP/2, and WordPress-related information were identified.                          |
| 5        | WAFW00F       | Detect the presence of a Web Application Firewall. | ModSecurity (SpiderLabs) was detected.                                                      |
| 6        | DNSRecon      | Enumerate the domain's DNS records.                | SOA, NS, A, MX, TXT, and SRV records were identified.                                       |

Note: The findings are based on the results obtained during the footprinting exercises.

## Security and Ethical Consideration 

All reconnaissance activities carried out in this project were conducted as part of the authorized NetworkWalks cybersecurity training program. The information gathered was used solely for educational purposes and to develop practical cybersecurity skills.
All reconnaissance and security testing activities should be performed only on systems for which proper authorization has been granted.


# Module 4 (WK2-PM4): Footprinting with theHarvester 


## Task 1: Email Address and Subdomain Enumeration Using theHarvester

### Command 
```txt
theHarvester -d microsoft.com -l 1000 -b baidu
```
### Purpose 
To gather publicly available email addresses and subdomains associated with a target organization for information gathering and reconnaissance.
### Evidence 
<img width="934" height="722" alt="Screenshot 2026-11-12 125929" src="https://github.com/user-attachments/assets/0adac1df-b4a5-44c6-93b9-99be271334f4" />
<img width="832" height="465" alt="Screenshot 2026-11-12 130013" src="https://github.com/user-attachments/assets/19a98a28-e598-40d7-92e5-f97968345f5b" />

## Task 2: Email Address and Subdomain Enumeration Using theHarvester (All Sources)

### Command 
```txt
theHarvester -d microsoft.com -l 50 -b all
```
### Purpose
To gather publicly available email addresses and subdomains associated with Microsoft using all available theHarvester data sources for reconnaissance.
### Evidence 
<img width="1061" height="887" alt="Screenshot 2026-11-12 131103" src="https://github.com/user-attachments/assets/736d4d5f-8cbc-4039-a60a-bce4eca5a8a6" />


# Module 5 (WK2-PM5): Network Scanning With Zenmap


## Task 1: Download & Install Zenmap 

Zenmap was downloaded and installed to provide a graphical interface for Nmap, making it easier to perform network scans, identify active hosts, and discover open ports and services.
```txt
https://nmap.org/download.html
```
### Evidence 
<img width="1428" height="821" alt="Screenshot 2026-11-12 014711" src="https://github.com/user-attachments/assets/7b455bf4-93dc-4315-9032-4a77963a12a9" />
<img width="923" height="664" alt="Screenshot 2026-11-12 014544" src="https://github.com/user-attachments/assets/4585e225-a097-4a0e-b8ca-441c034f7b0a" />

## Task 2: Local IP Address & LAN Subnet

The local IP address and LAN subnet were identified to understand the network configuration and determine the range of IP addresses available for scanning.
The network used for scan is 
```txt
LAN Subnet: 10.110.235.0/24
```
### Evidence 
<img width="1027" height="262" alt="Screenshot 2026-11-13 111139" src="https://github.com/user-attachments/assets/9397232c-48e7-4d63-bfd8-ec931ae238d
0" />

## Task 3: Identifying Live Hosts on the Local Network Using Zenmap

Zenmap was used to scan the local IP subnet and identify active hosts or devices connected to the network.
### Evidence 
<img width="1378" height="826" alt="Screenshot 2026-11-12 025038" src="https://github.com/user-attachments/assets/1a735600-58c4-4f51-ad25-34d557f94757" />

## Task 4: Number of Live Host 

The scan covered 256 IP address and identified:
```txt
2 live host
Therefore,
Total IP address scanned: 256
Live host discovered: 2
```

## Task 5: IP Addresses of Live Hosts  

The following ip address was discovered:
| IP Address      | Status   |
|-----------------|----------|
| 10.110.235.56   | Up       |
| 10.110.235.201  | Up       |

## Task 6: MAC Addresses of Live Hosts

Nmap discovered the MAC address for 10.110.235.56.
|IP Adress         | MAC Address       |
|------------------|-------------------|
| 10.110.235.56    | CA:1D:A7:F0:AD:05 |
| 10.110.235.201   | Not displayed     |

## Task 7: Zenmap Topology

Zenmap's Topology view was used to display the discovered hosts and their network connections.
The topology diagram was then exported as a PDF for documentation.
### Evidence 
<img width="1879" height="938" alt="Screenshot 2026-11-12 025014" src="https://github.com/user-attachments/assets/10a5ddf0-fb6c-4a71-a4e5-ade883003e7d" />

## Security and Ethical Consideration

The network scanning exercise was conducted within the authorized NetworkWalks training environment for educational purposes and to gain practical experience in network discovery and analysis.
All network scanning activities should be restricted to systems and networks for which proper authorization has been granted.


# Author 

Name: Yusuf Fatimah Itunuoluwa 

Program: Networkwalks Cybersecurity Internship


















































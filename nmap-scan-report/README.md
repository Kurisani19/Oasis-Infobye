Nmap Scan Report – Security Analyst Intern Task
Name: Kurisani Mbhungele
Position: Security Analyst Intern
Date: July 28, 2025

Task-1 Overview
As part of my internship and learning process in cybersecurity, I performed a basic network scan using Nmap, a widely used tool for discovering open ports and services on a machine. The goal was to identify potential vulnerabilities and understand how systems communicate over a network.

Tool Used
Tool Name: Nmap
Version: 7.97 (Windows version)
Command Used:nmap -A 192.168.8.118 > nmap_scan_results.txt
This command runs an advanced scan to check for open ports, services, and operating system information, then saves the output to a text file for analysis.

Target Information
Host IP Address: 192.168.8.118
Host Name: LAPTOP-IOS3HUQK
MAC Address: cc:47:40:e3:45:f7 (AzureWave Technology)
Operating System: Windows (based on detected services)
Uptime: Around 3 days
Distance: Local machine (0 hops)

Scan Results
These are the open ports and services I discovered:

Port	State	Service	Description
135/tcp	Open	msrpc	Used for Windows remote procedure calls
139/tcp	Open	netbios-ssn	NetBIOS for file and printer sharing
445/tcp	Open	microsoft-ds	SMB protocol, often used for file sharing

Note: The scan also showed that 997 other ports were closed.

What I Learned
Port 135 (msrpc)
This port helps Windows applications communicate across networks. It is essential but can be a risk if left open on untrusted networks. A firewall should be used to restrict access.

Port 139 (netbios-ssn)
This port is used for older Windows file sharing functions. It is common on local networks but should never be exposed to the internet.

Port 445 (microsoft-ds / SMB)
This port is used for file sharing through SMB. It is one of the most targeted ports by malware such as WannaCry. It must be protected and only accessible within trusted environments.

Security Notes
SMB message signing is enabled but not required. This configuration can allow attackers on the same network to intercept and modify SMB traffic through man-in-the-middle attacks.

Nmap was not able to determine the exact operating system. I learned that running the scan as an administrator or using the --osscan-guess option can help get better results.

Screenshot 
Below is a screenshot of the Nmap scan output as seen in the terminal

c:\Users\KURISANI\OneDrive\Desktop\nmap_output.png


Files Submitted
nmap_tscan_results.txt – Full scan output
nmap_output.png – Screenshot of scan
README.md – This report

Conclusion
This was my first hands-on experience using Nmap for network scanning. It helped me understand the importance of checking open ports and learning what services are running on a machine. I now see how important it is to protect certain services and properly configure systems to reduce risks.

I am excited to keep learning more about network security and vulnerability assessment during my internship.
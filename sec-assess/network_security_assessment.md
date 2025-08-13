 Network Security Assessment Report

**Author:** Kurisani Mbhungele  
**Date:** 2025-08-05  
**Tools Used:** Nmap, Wireshark  
**Network Range:** 172.18.48.0/20

 1. Introduction

This report documents a network security assessment performed on a local test network using Nmap and Wireshark tools. The goal was to identify live hosts, open ports, and any potential vulnerabilities.

 2. Methodology

 Nmap Scan:
- Conducted a stealth SYN scan (`-sS`) with service detection (`-sV`) and OS detection (`-O`).
- Targeted subnet: 172.18.48.0/20. 

 Wireshark Capture:
- Captured network traffic on interface `eth0`.
- Capture duration: approximately 10 minutes.

 3. Findings

 Nmap Results:
- Host detected at 172.18.48.1.
- All 1000 scanned ports were filtered, likely indicating active firewall filtering.
- OS detection inconclusive due to filtering.
- MAC address indicates Microsoft device.

 Wireshark Analysis:
- Traffic captured shows no cleartext credentials or suspicious activity.
- Network traffic mostly encrypted or normal operational data.
- No immediate security concerns observed.

 4. Recommendations

- Continue regular network monitoring.
- Verify firewall rules to ensure only necessary ports are open.
- Perform scans on additional subnets or devices for broader assessment.

 5. Conclusion

The network is currently well protected with firewall rules that filter all inbound port scans. No vulnerabilities were detected during this assessment.


 6. Attached Files

- `nmap_results.txt`
- `wireshark_capture.pcap`


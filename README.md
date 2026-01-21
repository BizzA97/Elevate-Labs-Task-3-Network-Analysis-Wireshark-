# Task 3 – Network Traffic Analysis using Wireshark

## Date
January 21, 2026

## Objective
The objective of this task is to understand how network traffic flows across a system and to analyze packets using Wireshark. This includes observing DNS queries, TCP connection establishment, and differences between plaintext and encrypted communication.

---

## Environment Details
- Operating System: Kali Linux (Kernel 6.12.13-amd64)
- Tool Used: Wireshark v4.4.4

---

## Task Overview
In this task, live network traffic was captured during a normal web browsing session. The captured packets were analyzed to identify core networking protocols and security mechanisms such as DNS resolution, TCP three-way handshake, and TLS encryption.

---

## Key Observations

### DNS Query Analysis
- DNS traffic was captured using protocol filters.
- The system resolved multiple Mozilla-related domains such as:
  - contile.services.mozilla.com
  - push.services.mozilla.com
  - content-signature-2.cdn.mozilla.net
- These queries help the browser locate backend services and content delivery networks before communication begins.

### TCP Three-Way Handshake
- The TCP connection setup process was clearly observed.
- The following sequence was identified:
  - SYN packet sent by the host
  - SYN-ACK response from the server
  - ACK packet completing the connection
- This confirms reliable connection establishment before data transmission.

### HTTP vs HTTPS (TLS)
- Some plaintext HTTP traffic was observed during infrastructure-related operations such as OCSP checks.
- HTTP traffic revealed readable information like host headers and user-agent strings.
- Actual web browsing traffic was protected using TLS encryption.
- Encrypted application data appeared unreadable after the TLS handshake.
- Certificates issued by Let's Encrypt and Internet Security Research Group confirmed secure communication.

---

## Files Included in This Repository
- `task3_kali_capture.pcapng` – Packet capture file
- `Network_Traffic_Analysis_Report.docx` – Detailed analysis report
- `screenshots/` – Evidence of packet capture and filtering
- `README.md` – Task overview and explanation

---

## Conclusion
This task demonstrated how packet sniffing and traffic analysis work in real environments. While some initial network communication is visible, secure browsing data remains protected through TLS encryption. The analysis confirms that essential networking and security protocols are functioning correctly on the system.

---

## Key Concepts Learned
- Packet sniffing
- DNS resolution
- TCP three-way handshake
- Difference between HTTP and HTTPS
- Importance of encryption in network security

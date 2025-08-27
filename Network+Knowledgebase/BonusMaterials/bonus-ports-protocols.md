# 📘 Bonus: Ports & Protocols Quick Sheet  

A **quick reference guide** for common CompTIA Network+ exam ports and protocols.  
Organized by category for **fast lookup**.  

---

## 🌐 Web & Remote Access  

| Service | Port(s) | Protocol | Notes |  
|---------|---------|----------|-------|  
| HTTP | 80 | TCP | Insecure web traffic |  
| HTTPS | 443 | TCP | Secure web traffic (TLS/SSL) |  
| SSH | 22 | TCP | Secure remote shell (replaces Telnet) |  
| Telnet | 23 | TCP | Insecure remote shell, deprecated |  
| RDP | 3389 | TCP | Remote Desktop Protocol |  

---

## 📧 Email & Messaging  

| Service | Port(s) | Protocol | Notes |  
|---------|---------|----------|-------|  
| SMTP | 25, 587, 465 | TCP | Email sending (465/587 = secure) |  
| IMAP | 143, 993 | TCP | Email retrieval (993 = secure) |  
| POP3 | 110, 995 | TCP | Email retrieval (995 = secure) |  

---

## 📡 Infrastructure Services  

| Service | Port(s) | Protocol | Notes |  
|---------|---------|----------|-------|  
| DNS | 53 | UDP/TCP | Name resolution |  
| DHCP | 67/68 | UDP | Dynamic IP allocation |  
| SNMP | 161/162 | UDP | Network management (v3 = secure) |  
| NTP | 123 | UDP | Time synchronization |  
| LDAP | 389 | TCP/UDP | Directory services (unencrypted) |  
| LDAPS | 636 | TCP | Secure directory services |  

---

## 🛠️ File Transfer  

| Service | Port(s) | Protocol | Notes |  
|---------|---------|----------|-------|  
| FTP | 20/21 | TCP | File transfer (insecure) |  
| FTPS | 990 | TCP | FTP over TLS/SSL (secure) |  
| SFTP | 22 | TCP | File transfer over SSH (secure) |  
| TFTP | 69 | UDP | Trivial FTP (no authentication) |  

---

⚡ Use this sheet for **memorization, quick review, and troubleshooting reference**.  

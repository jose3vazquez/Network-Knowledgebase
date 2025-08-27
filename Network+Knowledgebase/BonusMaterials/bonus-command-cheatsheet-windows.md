# 📘 Bonus: Command Cheat Sheet (Windows)

## Networking Basics  
| Command | Description | Example |  
|---------|-------------|---------|  
| `ipconfig` | Display basic IP config | `ipconfig` |  
| `ipconfig /all` | Show full config (MAC, DNS, DHCP) | `ipconfig /all` |  
| `ipconfig /release` | Release DHCP lease | `ipconfig /release` |  
| `ipconfig /renew` | Renew DHCP lease | `ipconfig /renew` |  

## Connectivity Tests  
| Command | Description | Example |  
|---------|-------------|---------|  
| `ping` | Test connectivity | `ping 8.8.8.8` |  
| `tracert` | Trace route to host | `tracert google.com` |  
| `pathping` | Ping + traceroute + loss stats | `pathping 8.8.8.8` |  

## Name Resolution  
| Command | Description | Example |  
|---------|-------------|---------|  
| `nslookup` | Query DNS records | `nslookup example.com` |  

## TCP/UDP Info  
| Command | Description | Example |  
|---------|-------------|---------|  
| `netstat -an` | Show active connections | `netstat -an` |  
| `netstat -rn` | Show routing table | `netstat -rn` |  

## Advanced  
| Command | Description | Example |  
|---------|-------------|---------|  
| `arp -a` | Show ARP table | `arp -a` |  
| `nbtstat -n` | Show NetBIOS info | `nbtstat -n` |  
| `telnet` | Test TCP ports (deprecated, must enable) | `telnet mail.example.com 25` |  

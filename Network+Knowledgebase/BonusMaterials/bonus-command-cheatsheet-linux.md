# 📘 Bonus: Command Cheat Sheet (Linux)

## Networking Basics  
| Command | Description | Example |  
|---------|-------------|---------|  
| `ifconfig` | Show interface config (legacy) | `ifconfig eth0` |  
| `ip addr` | Show IP addresses (modern) | `ip addr show` |  
| `ip link` | Show interfaces (link-layer) | `ip link show` |  
| `ip route` | Show routing table | `ip route show` |  

## Connectivity Tests  
| Command | Description | Example |  
|---------|-------------|---------|  
| `ping` | Test connectivity | `ping 8.8.8.8` |  
| `traceroute` | Trace route to host | `traceroute google.com` |  
| `mtr` | Continuous traceroute | `mtr google.com` |  

## Name Resolution  
| Command | Description | Example |  
|---------|-------------|---------|  
| `dig` | Detailed DNS query | `dig example.com ANY` |  
| `host` | Simple DNS lookup | `host example.com` |  
| `nslookup` | Query DNS (like Windows) | `nslookup example.com` |  

## TCP/UDP Info  
| Command | Description | Example |  
|---------|-------------|---------|  
| `netstat -tulnp` | Show listening ports + PIDs | `netstat -tulnp` |  
| `ss -tuln` | Modern replacement for netstat | `ss -tuln` |  
| `lsof -i :80` | Show process using port 80 | `lsof -i :80` |  

## Packet Capture & Analysis  
| Command | Description | Example |  
|---------|-------------|---------|  
| `tcpdump -i eth0` | Capture traffic | `tcpdump -i eth0` |  
| `tcpdump port 80` | Filter by port | `tcpdump port 80` |  

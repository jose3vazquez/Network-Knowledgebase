# 📘 Bonus: Troubleshooting Scenarios  

A set of **realistic troubleshooting case studies** with **step-by-step fixes**, aligned with CompTIA Network+ exam objectives.  

---

## 1. DNS Resolution Failure  
**Symptom:** Users can’t browse websites by name but can reach them by IP.  
**Steps:**  
1. Verify IP connectivity with `ping 8.8.8.8`.  
2. Test DNS resolution with `nslookup google.com`.  
3. Check client DNS settings (static vs DHCP).  
4. Verify DNS server availability.  
5. Restart DNS service or reconfigure to secondary DNS.  
✅ **Fix:** Point clients to working DNS servers (e.g., 8.8.8.8 / 1.1.1.1).  

---

## 2. Slow Wireless Network  
**Symptom:** Wi-Fi is sluggish and dropping connections.  
**Steps:**  
1. Check signal strength and SNR with wireless analyzer.  
2. Inspect channel overlap (2.4 GHz often crowded).  
3. Move clients/APs to 5 GHz band.  
4. Reduce AP overload by adding additional APs.  
5. Update AP firmware.  
✅ **Fix:** Change channels and balance client load across APs.  

---

## 3. Intermittent Connectivity on Switch Port  
**Symptom:** User PC connects/disconnects randomly.  
**Steps:**  
1. Check cable integrity (wiggle test, replace cable).  
2. Test with `ping -t <gateway>` to watch drops.  
3. Verify port speed/duplex (autoneg vs manual).  
4. Check for errors with `show interface` on switch.  
✅ **Fix:** Replace bad cable, set port to correct duplex/speed.  

---

## 4. Printer Not Reachable Over Network  
**Symptom:** Users can’t print; jobs stuck in queue.  
**Steps:**  
1. Ping printer IP.  
2. Check if IP changed (DHCP vs static).  
3. Restart print spooler service.  
4. Ensure firewall isn’t blocking port 9100 (RAW).  
✅ **Fix:** Assign static IP, update DNS/print server entry.  

---

## 5. IP Conflict Detected  
**Symptom:** Two devices lose connectivity when online together.  
**Steps:**  
1. Run `arp -a` to check duplicate MAC for same IP.  
2. Trace cabling to identify conflicting device.  
3. Reconfigure one device with new IP.  
✅ **Fix:** Reserve IPs in DHCP to avoid future conflicts.  

---

## 6. High Latency in VoIP Calls  
**Symptom:** Choppy audio, jitter, or one-way voice.  
**Steps:**  
1. Measure delay, jitter, and packet loss.  
2. Verify QoS is applied on routers/switches.  
3. Prioritize VoIP VLAN traffic.  
4. Reduce bandwidth-hog apps (streaming, backups).  
✅ **Fix:** Apply QoS, dedicate VLAN, increase bandwidth.  

---

## 7. VPN Connection Fails  
**Symptom:** Remote users can’t establish VPN.  
**Steps:**  
1. Confirm internet connectivity.  
2. Test DNS resolution of VPN gateway.  
3. Verify user credentials + MFA.  
4. Check VPN client logs.  
5. Inspect firewall ports (IPsec: 500/4500, SSL: 443).  
✅ **Fix:** Open required ports and verify VPN config.  

---

## 8. Broadcast Storm on LAN  
**Symptom:** Network slows dramatically, CPU spikes on switches.  
**Steps:**  
1. Check switch logs for broadcast/multicast flood.  
2. Run `show spanning-tree` to detect loop.  
3. Identify mispatched cable (loop).  
4. Enable storm control on switches.  
✅ **Fix:** Remove loop, enable STP.  

---

## 9. Website Unreachable from Internal Network  
**Symptom:** Users can access other sites but not a specific one.  
**Steps:**  
1. Ping site from external network (rule out outage).  
2. Trace route to see where it fails.  
3. Inspect firewall/web filter logs.  
4. Whitelist the domain if mistakenly blocked.  
✅ **Fix:** Adjust firewall/web filter policies.  

---

## 10. Rogue Access Point Detected  
**Symptom:** Users connect to “Company-WiFi” but report no access or stolen credentials.  
**Steps:**  
1. Use wireless scanner to identify rogue SSID.  
2. Trace MAC address to switch port.  
3. Disable the port or physically remove AP.  
4. Educate users on verifying secure SSID.  
✅ **Fix:** Remove rogue AP and enforce WPA3 with 802.1X.  

---

⚡ These scenarios give **hands-on practice** in applying Network+ troubleshooting methodology, bridging the gap between theory and real-world problem solving.  

# 📘 Bonus: Subnetting Practice

## Subnetting Basics  
- **CIDR notation** expresses how many bits are network (e.g., /24 = 255.255.255.0).  
- **Usable hosts per subnet** = 2^(host bits) − 2 (network + broadcast).  
- **Subnetting table (common sizes):**  

| CIDR | Subnet Mask      | # of Hosts | Example Subnet                |  
|------|-----------------|------------|-------------------------------|  
| /24  | 255.255.255.0   | 254        | 192.168.1.0 – 192.168.1.255  |  
| /25  | 255.255.255.128 | 126        | 192.168.1.0 – 192.168.1.127  |  
| /26  | 255.255.255.192 | 62         | 192.168.1.0 – 192.168.1.63   |  
| /27  | 255.255.255.224 | 30         | 192.168.1.0 – 192.168.1.31   |  
| /28  | 255.255.255.240 | 14         | 192.168.1.0 – 192.168.1.15   |  

---

## Practice Problems  

1. **Given 192.168.50.0/27:**  
   - How many subnets? → 8  
   - How many usable hosts per subnet? → 30  

2. **Given 10.0.0.0/16:**  
   - How many usable hosts? → 65,534  
   - First usable? → 10.0.0.1  
   - Last usable? → 10.0.255.254  

3. **You need at least 500 hosts per subnet. Which mask?**  
   - /23 → 510 usable hosts.  

4. **A company has 192.168.100.0/24 and needs 6 subnets. What mask?**  
   - /27 → 8 subnets possible, 30 usable each.  

---

## Quick Tips & Tricks  

- **Shortcut memory rule:**  
  - /30 = 2 usable  
  - /29 = 6 usable  
  - /28 = 14 usable  
  - /27 = 30 usable  
  - /26 = 62 usable  
  - /25 = 126 usable  
  - /24 = 254 usable  

- Always remember: **more subnet bits → fewer hosts**.  

---

⚡ This file is designed as a **practice & reference pack** — compact, actionable, and exam-relevant.  

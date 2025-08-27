# 📘 Bonus: Network Diagrams (Hybrid)

This file includes **ASCII/Markdown topology sketches** that render natively on GitHub for quick study, **plus placeholders** for you to drop in polished PNG/SVG diagrams later (e.g., from draw.io or Excalidraw).

> To add images later: export to `/diagrams/<name>.png` and replace the placeholders below.

---

## 1) Small Office LAN (Star Topology)

```text
             [Internet]
                 |
             [ISP Modem]
                 |
              (Router)
                 |
              (Switch)
      /-----/---/---\-----\
   [PC1] [PC2] [NAS] [Printer] ... [VoIP]
```

**Image placeholder:** `![Small Office LAN](diagrams/lan-small-office.png)`

---

## 2) VLAN Segmentation on a Managed Switch

```text
                   (Layer-3 Switch)
                /------ VLAN 10 ------\
               /                       \
          [PC1]--(Port 1)           (Port 3)--[PC3]
               \                       /
                \----- VLAN 20 ------/
                          |
                       (Port 2)
                         [PC2]

- VLAN 10 = STAFF
- VLAN 20 = GUEST
- Inter-VLAN routing via L3 switch (SVIs)
```

**Image placeholder:** `![VLAN Segmentation](diagrams/vlan-segmentation.png)`

---

## 3) WLAN with Controller + Multiple APs (Campus)

```text
                   [Core Router]
                        |
                     (Firewall)
                        |
                   [WLC Controller]
                     /     |     \
                 [AP1]  [AP2]  [AP3]       <-- APs on PoE switches
                   |       |       |
                ~ Wi-Fi ~ Wi-Fi ~ Wi-Fi ~   (SSID: campus-secure, campus-guest)
```

**Image placeholder:** `![WLAN with Controller](diagrams/wlan-controller-aps.png)`

---

## 4) Site-to-Site VPN (Branch to HQ)

```text
[Branch LAN]--(Branch Router)===< IPsec Tunnel >===(HQ Router)--[HQ LAN]
     |                                                          |
   (Sw1)                                                    (Core Sw)
```

Legend: `===` encrypted tunnel (IPsec), `--` unencrypted link.

**Image placeholder:** `![Site-to-Site VPN](diagrams/s2s-vpn.png)`

---

## 5) DMZ with Public-Facing Services

```text
            [Internet]
                |
             (Edge FW)
          /-------------\
         /               \
     [DMZ Net]        [Internal Net]
      /     \             |
 [Web]     [Mail]       (Core FW)
                          |
                        [AD/DB]
```

- Edge firewall separates **Internet ↔ DMZ**
- Core/inside firewall separates **DMZ ↔ Internal**

**Image placeholder:** `![DMZ Design](diagrams/dmz-two-tier.png)`

---

## 6) High Availability Pair (FW/Router HA)

```text
           [Internet]
               |
         +--------------+
         | FW-A (Active)|
         +--------------+
               ||  <-- HA link (heartbeat/state sync)
         +--------------+
         | FW-B (Standby)|
         +--------------+
               |
            (Switch)
          /    |     \
       [Srv1][Srv2][Srv3]
```

**Image placeholder:** `![Firewall HA](diagrams/firewall-ha.png)`

---

## 7) IDS/IPS + SPAN (Port Mirroring)

```text
        (Switch)
        /  |   \
     [Srv][PC] (SPAN)---->[IDS/IPS Sensor]
```

- SPAN/mirror port copies traffic to the IDS/IPS sensor.

**Image placeholder:** `![SPAN to IDS](diagrams/span-ids.png)`

---

## 8) Hub-and-Spoke WAN (MPLS/SD-WAN)

```text
               [Data Center / Hub]
                       |
                 (Provider Cloud)
                 /      |       \
             [Branch1][Branch2][Branch3]
```

- Could be MPLS or SD‑WAN overlay with centralized control plane.

**Image placeholder:** `![Hub-and-Spoke WAN](diagrams/wan-hub-spoke.png)`

---

## 9) Remote Access VPN (AnyConnect/SSL VPN)

```text
[Remote User Laptop] ==TLS/SSL==> (VPN Gateway) -- (Firewall) -- [Internal Apps]
                     MFA/Certs
```

**Image placeholder:** `![Remote Access VPN](diagrams/ra-vpn.png)`

---

## 10) Basic Redundant Links with STP

```text
      (Switch A)====(Switch B)
           ||         ||
          [PC1]     [PC2]

- `====` indicates a redundant uplink.
- STP blocks one link to prevent Layer 2 loops; auto‑unblocks on failure.
```

**Image placeholder:** `![STP Redundancy](diagrams/stp-redundancy.png)`

---

## Notes for Polished Diagrams

- Create a `/diagrams/` folder at repo root.  
- Export drawings as **SVG** (preferred, crisp at any zoom) or **PNG** (fallback).  
- Keep filenames short and meaningful (e.g., `lan-small-office.svg`).  
- Reference them using Markdown `![Alt Text](diagrams/name.svg)`.  
- Optional: include the **source** diagram files (`.drawio` or `.excalidraw`) in `/diagrams/src/` for future edits.

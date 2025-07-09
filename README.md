# 🛰️ Dynamic Routing using RIP v2 (Classless IP – Multi-Router Setup)

This project demonstrates **dynamic routing using RIP version 2** on a classless network (CIDR) using **5 interconnected routers** in Cisco Packet Tracer.

---

## 📁 File Included

- `Dynamic-Routing-RIP.pkt` — Cisco Packet Tracer project with RIP v2 configuration and classless IP addressing.

---

## 🧠 Project Summary

- **Routing Protocol:** RIP v2 (dynamic)
- **IP Addressing:** Classless (CIDR) using `10.0.128.0/28` and its subnets
- **Topology:** 5 routers, multiple end devices
- **Route Complexity:**
  - One PC reaches another via **2-hop path**
  - Another PC reaches via **3-hop path**

---

## 🌐 Network Topology Highlights

- Base Network: `10.0.128.0/28` (CIDR)
- Subnetted for point-to-point and LAN links
- 5 Routers interconnected in a semi-linear structure
- End devices (PCs) connected at edge routers
- RIP v2 distributes routes dynamically

📷 **Topology Screenshot:**
![Topology](/topology.png)

---

## ⚙️ RIP v2 Configuration (Sample per Router)

All routers are configured similarly with classless networks.

```bash
enable
configure terminal
router rip
 version 2
 no auto-summary
 network 10.0.128.0
 network 10.0.128.16
 network 10.0.128.32
... (as per router’s connected subnets)

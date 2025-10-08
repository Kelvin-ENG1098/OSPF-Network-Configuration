# 🛰️ OSPF Network Configuration Project

## 📘 Overview
This project demonstrates the configuration and verification of **Open Shortest Path First (OSPF)** dynamic routing in a multi-router network topology.  
It simulates a small enterprise network where routers automatically share routing information to maintain connectivity between multiple subnets.

---

## 🧩 Network Topology
The network consists of multiple routers, switches, and end devices connected to form a routed domain using **OSPFv2**.

**Devices Used:**
- 3 × Huawei Routers (e.g., AR series)
- 2 × Layer 2 Switches
- 3 × End Devices (PCs)
- 1 × Server

**Routing Protocol:** OSPFv2  
**Area Type:** Single Area (Area 0)

---

## ⚙️ Configuration Summary

| Device | Process ID | Networks Advertised | Area |
|---------|-------------|--------------------|------|
| R1 | 1 | 10.0.0.0/24, 192.168.1.0/24 | 0 |
| R2 | 1 | 192.168.2.0/24, 172.16.1.0/24 | 0 |
| R3 | 1 | 172.16.2.0/24, 192.168.3.0/24 | 0 |

**Key Tasks Performed:**
- Enabled OSPF on each router interface.
- Verified adjacency formation using `show ip ospf neighbor`.
- Checked route propagation using `show ip route ospf`.
- Confirmed connectivity between remote subnets via `ping`.

---

## 🧠 Learning Objectives
- Understand and implement **dynamic routing** using OSPF.
- Verify **neighbor relationships** and **link-state advertisements (LSAs)**.
- Observe **route propagation** between routers.
- Test **end-to-end network reachability** across multiple subnets.

---

## 🧾 Verification Commands
```bash
show ip ospf neighbor
show ip ospf interface brief
show ip route ospf
ping <destination-IP>

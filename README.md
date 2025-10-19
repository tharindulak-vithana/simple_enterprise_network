# Simple Enterprise Network – Cisco Packet Tracer Project

## Project Overview
This is an **Enterprise Network Simulation** built using **Cisco Packet Tracer**.  
The project demonstrates how a typical enterprise network is structured with **multiple routing domains**, **Access Control Lists (ACL)**, and **Network Address Translation (NAT)** for controlled and secure Internet access.

---

## Project Objectives
-  Build a structured multi-segment enterprise network.  
-  Implement **OSPF** & **RIP** routing protocols to enable inter-network connectivity.  
-  Configure **ACL (Access Control List)** to permit **ICMP traffic only**.  
-  Use **NAT (Network Address Translation)** to allow internal hosts to access external networks through the ISP.  
-  Verify connectivity between internal and external segments with proper access control.

---

## Network Topology

**Routing Protocols:**
- 🟩 OSPF – Main backbone (10.0.1.0 / 10.0.2.0 / 10.0.3.0 segments)  
- 🟨 RIP – Secondary area (10.0.4.0 / 10.0.5.0 segments)

**LAN Segments:**
- PC0 → 192.168.1.0/24  
- PC1 → 192.168.2.0/24  
- PC2 → 172.16.1.0/24

**WAN / Inter-Router Networks:**
- 10.0.1.0 / 10.0.2.0 / 10.0.3.0 / 10.0.4.0 / 10.0.5.0

**Security & Internet Access:**
-  ACL configured to allow only ICMP traffic between networks.
-  NAT configured on the edge router to connect LAN to ISP.

---

## ⚙️ Key Configurations

### Routing
- OSPF between core routers (Router8, RouterFT, Router3, Router11)
- RIP between RouterFT, Router5, Router6
- Default route towards ISP


### Access Control List (ACL)
- Standard / Extended ACL used to allow **ICMP (ping)** traffic only.
- All other unwanted traffic types are denied.
- ACL applied to outbound interface on the edge router (RouterFT).


### NAT Configuration
- NAT Overload (PAT) implemented on the ISP-facing router.
- Allows multiple internal devices to share one public IP.
- Verifies Internet reachability without exposing internal IP addresses.

---

## Devices Used
-  Cisco 2911 Routers × 6  
-  Switches × 2  
-  PCs × 6
-  Laptops × 2  
-  ISP Router × 1
-  Servers × 3
-  Printer × 1

---

## 📂 Project Files
- `simple_enterprise_network.pkt` → Main Cisco Packet Tracer project
- `README.md` → Documentation file

---

## How to Explore the Project
1. Open the `.pkt` file using Cisco Packet Tracer.  
2. View router configurations (OSPF, RIP, NAT, ACL).  
3. Use `ping` command between PCs and ISP to verify ACL and NAT functionality.  
4. Observe that only **ICMP traffic is allowed** through the edge router.  
5. Modify ACL or NAT rules to experiment with network security behavior.

---

## Future Enhancements
- Add DHCP server for dynamic IP assignment  
- Configure VLANs for departmental segmentation  
- Add firewall features with extended ACLs  
- Implement redundancy / failover routes  

---

## Author
  `tharindulak-vithana`

---

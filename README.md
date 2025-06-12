# Home-Network
Building a home Network using cisco
### **Network Configuration & Testing Project**  
**Role:** SOC Analyst (Hands-On Networking Lab)  
**Tools Used:** Cisco Packet Tracer, Physical Networking Devices (Switch, Laptops), Command Line (ipconfig, ping, nslookup)  

---

### **Project Overview**  
As part of foundational SOC training, this project involved designing, configuring, and testing a basic **local area network (LAN)** to understand core networking principles critical for security monitoring. The lab included both **virtual (Packet Tracer)** and **physical device configurations**, emphasizing IP addressing, connectivity testing, and troubleshooting—key skills for analyzing network traffic and detecting anomalies in a SOC environment.  

---

### **Key Tasks Performed**  
1. **Network Topology Setup**  
   - Deployed a **Cisco 3650 switch** and connected two endpoints (Laptop1 and Laptop2) using Ethernet cables.  
   - Compared virtual (Packet Tracer) and physical setups to validate real-world applicability.  

2. **IP Addressing & Configuration**  
   - Assigned **static IPv4 addresses** to endpoints:  
     - Laptop1: `192.168.1.1/24`  
     - Laptop2: `192.168.1.2/24`  
   - Configured **subnet masks** (`255.255.255.0`) and **default gateways** (`192.168.1.254`) manually (simulating a non-DHCP environment).  

3. **Connectivity Validation**  
   - Used `ipconfig` and `ipconfig /all` to verify IP/MAC addresses.  
   - Tested communication between devices using **ICMP ping**:  
     ```bash
     ping 192.168.1.2  # From Laptop1 to Laptop2
     ```  
   - Analyzed successful replies (echo requests/replies) to confirm network functionality.  

4. **DNS & Name Resolution**  
   - Demonstrated **nslookup** to resolve domain names (e.g., `google.com`) to IP addresses, highlighting the role of DNS in network traffic analysis.  

5. **Physical vs. Virtual Comparison**  
   - Replicated the Packet Tracer lab on physical devices (C9200CX switch, USB-to-Ethernet adapters for modern laptops) to troubleshoot real-world constraints (e.g., missing Ethernet ports).  

---

### **SOC-Relevant Skills Demonstrated**  
- **Network Segmentation**: Configured devices in the same subnet to understand broadcast domains.  
- **Traffic Analysis**: Used ping to simulate and monitor basic traffic flows (foundational for detecting outages or MITM attacks).  
- **Endpoint Hardening**: Disabled DHCP to enforce static IPs (common in secure environments).  
- **Troubleshooting**: Identified misconfigurations (e.g., incorrect subnet masks) through failed pings.  

---

### **Tools & Commands Mastered**  
| **Tool/Command**       | **Purpose**                                  |  
|-------------------------|----------------------------------------------|  
| Cisco Packet Tracer     | Network simulation and visualization         |  
| `ipconfig`/`ifconfig`   | Verify IP/MAC addresses and DHCP status      |  
| `ping`                  | Test connectivity and latency                |  
| `nslookup`              | Investigate DNS resolution issues            |  
| Physical cabling        | Validate layer-1 (physical) connectivity     |  

---

### **Why This Matters for SOC Roles**  
- **Incident Detection**: Understanding normal network behavior (e.g., successful pings) is critical to identifying anomalies (e.g., failed pings due to ARP spoofing).  
- **Forensic Analysis**: Static IP logs aid in tracking devices during investigations.  
- **SIEM Integration**: Raw network data (e.g., ping logs) can feed into SIEM tools like Splunk for correlation.  

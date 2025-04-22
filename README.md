
# 🧪 Exercise 1: Basic Network Setup & Connectivity

## 🎯 Goal  
Build a simple topology, configure essential device settings, assign IP addresses, and verify basic intra- and inter-network connectivity.

---

## 🖥️ Topology Components

- **1 Router**: Cisco 2911  
- **2 Switches**: Cisco 2960  
- **4 PCs**: Two per switch  

**Connections:**  
- PCs → Switches  
- Switches → Router  
  - Router `Gi0/0` ↔ Switch `SW1`  
  - Router `Gi0/1` ↔ Switch `SW2`  

---

## 🧾 IP Addressing Plan

| Network    | Device | Interface | IP Address         | Subnet Mask       | Gateway        |
|------------|--------|-----------|--------------------|-------------------|----------------|
| Network A  | Router | Gi0/0     | 192.168.10.1       | 255.255.255.0     | —              |
| Network A  | PC1    | —         | 192.168.10.10      | 255.255.255.0     | 192.168.10.1   |
| Network A  | PC2    | —         | 192.168.10.11      | 255.255.255.0     | 192.168.10.1   |
| Network B  | Router | Gi0/1     | 192.168.20.1       | 255.255.255.0     | —              |
| Network B  | PC3    | —         | 192.168.20.10      | 255.255.255.0     | 192.168.20.1   |
| Network B  | PC4    | —         | 192.168.20.11      | 255.255.255.0     | 192.168.20.1   |

---

## 📝 Tasks

1. **Build the Topology** in Packet Tracer.

2. **Set Hostnames**:
   - Router: `R1`
   - Switches: `SW1`, `SW2`

3. **Secure Access**:
   - Configure `enable secret`
   - Set `console` and `vty` passwords

4. **Router Interface Setup**:
   - Assign IPs to `Gi0/0` and `Gi0/1`
   - Use `no shutdown` to enable interfaces

5. **PC Configuration**:
   - Set static IP addresses and default gateways

6. **Add Interface Descriptions**:
   - Example: `description Link to SW1` on router interface `Gi0/0`

---

## ✅ Verification

- [x] PCs in **Network A** can ping each other  
- [x] PCs in **Network B** can ping each other  
- [x] All PCs can ping their **default gateway**  
- [x] PCs in **Network A and B** can ping each other through the router (via directly connected routing)  


![Screenshot 2025-04-22 135941](https://github.com/user-attachments/assets/3234e0e8-ad5a-4506-8234-2dd47ae17d81)

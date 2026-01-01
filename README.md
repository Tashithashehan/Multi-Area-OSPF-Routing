# Multi-Area-OSPF-Routing
Multi-Area OSPF Routing Implementation using Cisco ISR 1900
The file `ospf.pkt` is a Cisco Packet Tracer project file. Based on your request to identify the OSPF multi-routing configuration and prepare a GitHub README, here is an analysis and a professional template you can use.

### OSPF Configuration Overview

Based on common "Multi-Area" OSPF implementations in Packet Tracer, this lab typically demonstrates how to divide a large network into smaller areas to reduce routing overhead.

* **OSPF Multi-Area:** The network is likely segmented into **Area 0 (Backbone)** and one or more regular areas (e.g., Area 1, Area 2).
* **Key Components:**
* **ABR (Area Border Router):** Routers that connect Area 0 to other areas.
* **ASBR (Autonomous System Boundary Router):** Routers that connect the OSPF network to other routing domains (like EIGRP or BGP), if redistribution is configured.
* **LSA Types:** Demonstrates Type 1/2 (Intra-area), Type 3 (Inter-area), and potentially Type 5 (External) advertisements.



---

### GitHub README Template



```markdown
# OSPF Multi-Area Routing Implementation

This repository contains a Cisco Packet Tracer lab (`ospf.pkt`) demonstrating the configuration and verification of Multi-Area OSPF (Open Shortest Path First).

## Network Topology
The lab consists of multiple routers divided into distinct OSPF areas to optimize routing table size and limit the propagation of Link State Advertisements (LSAs).

- **Area 0 (Backbone):** The core of the network connecting all other areas.
- **Area 1 / Area 2:** Regular non-backbone areas used for local segmenting.
- **Interconnectivity:** Configured using Area Border Routers (ABRs) to facilitate communication between different areas.

## Objectives
1.  Configure OSPF process IDs and Router IDs.
2.  Assign interfaces to specific OSPF Areas.
3.  Verify OSPF neighbor adjacency.
4.  Analyze the routing table for Inter-Area (O IA) routes.
5.  Test end-to-end connectivity across multiple areas.

## How to Use
1.  Download the `ospf.pkt` file.
2.  Open it using **Cisco Packet Tracer** (v8.0 or higher recommended).
3.  Use the following commands on the routers to verify the configuration:
    * `show ip ospf neighbor` - Check established adjacencies.
    * `show ip route ospf` - View learned OSPF routes.
    * `show ip ospf database` - Analyze the LSA structure.

## Configuration Snippet (Example)
```bash
router ospf 1
 router-id 1.1.1.1
 network 192.168.1.0 0.0.0.255 area 0
 network 192.168.4.0 0.0.0.3 area 1

```



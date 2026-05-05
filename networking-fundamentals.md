# TryHackMe — What is Networking?

**Path:** Cyber Security 101  
**Platform:** TryHackMe  
**Completed:** May 2025  
**Difficulty:** Beginner  

---

## What is Networking?

A network is two or more devices connected together to share resources — files, internet access, printers, etc.

Networks can be:
- **LAN (Local Area Network)** — small, e.g. home or office
- **WAN (Wide Area Network)** — large, e.g. connecting cities or countries

---

## What is the Internet?

The internet is a network of networks — thousands of LANs and WANs connected together globally.

- Originated from **ARPANET** (1960s US military project)
- Data travels across the internet in packets, routed between devices

---

## Identifying Devices on a Network

Every device on a network needs a unique identifier:

**IP Address**
- Logical address assigned to a device
- Can change (especially with DHCP)
- Example: `192.168.1.1`
- Two versions: IPv4 (32-bit) and IPv6 (128-bit)

**MAC Address**
- Physical address burned into the network interface card (NIC)
- Permanent and unique per device
- Example: `a4:c3:f0:85:ac:2d`
- First 3 pairs = manufacturer, last 3 pairs = device ID

---

## Ping (ICMP)

Ping tests whether a device is reachable on a network.

- Uses **ICMP (Internet Control Message Protocol)**
- Sends an **echo request**, expects an **echo reply**
- Measures round-trip time in milliseconds

```bash
ping 192.168.1.1
ping google.com
```

**TTL (Time to Live)** — each hop across a router decrements TTL by 1. When TTL hits 0 the packet is dropped. Prevents packets looping forever.

**SOC relevance:** Ping is a basic reachability check. No reply can mean the host is down, blocking ICMP, or a network path is broken.

---

## Key Takeaways

- IP = logical, changeable. MAC = physical, permanent.
- The internet is ARPANET's descendant — a network of networks
- Ping/ICMP is the first tool to check if a host is alive
- TTL reveals network distance and is used in OS fingerprinting

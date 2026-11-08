# BoardNet: Board Examination Communication Network

A network simulation built in Cisco Packet Tracer for the CSE course. It connects six HSC education boards of Bangladesh (Dhaka, Rajshahi, Chattogram, Barishal, Sylhet, Khulna) into one secure network.

## Topology

<img width="1919" height="908" alt="image" src="https://github.com/user-attachments/assets/8251768b-c18a-4854-8c1b-adfb88a1f514" />

## What it does

- **VLSM subnetting:** one /16 base network divided across the six board networks
- **DHCP:** the Dhaka router serves Dhaka, Chattogram, Sylhet, and Rajshahi, while Khulna and Barishal run their own DHCP servers
- **DNS and web:** a central DNS server in Dhaka, with www.dhk.edu.bd and www.ctg.edu.bd reachable from every board
- **Email:** a local mail server for each board (mail.dhk.edu.bd, mail.ctg.edu.bd, etc.)
- **Routing:** RIP between Dhaka, Sylhet, and Rajshahi, a default route on Chattogram, and static routes on Khulna and Barishal
- **Redundancy:** Khulna and Barishal still reach the network through each other if their direct link to Dhaka goes down

## Tech used

- Cisco Packet Tracer

## How to open

1. Download the `.pkt` file from this repo.
2. Open it with Cisco Packet Tracer.

## My contribution

I designed and configured the full network on my own, including:

- VLSM subnetting and the IP addressing plan
- Router configuration for all six boards
- DHCP, DNS, web, and email server setup
- RIP, static, and default routing, plus the redundancy links between Khulna and Barishal
- Testing: ping between all devices, website access, and link failover

## Course

CSE, BRAC University

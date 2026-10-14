# Lab 01 — Introduction to Networking Devices and Network Topology

## Objective

I completed this lab to identify common networking devices, understand their roles, and build a network topology in Cisco Packet Tracer.

The exercise required me to select, position, and connect network devices. Device configuration and connectivity testing were not objectives of this lab.

## Tools

- Cisco Packet Tracer

## Devices Used

| Device | Model / Type | Quantity |
|---|---|---|
| Router | Cisco 2911 | 2 |
| Switch | Cisco 2960 | 2 |
| Firewall | Cisco ASA 5505 | 2 |
| Client | PC | 2 |
| Server | Server | 2 |
| Attacker device | Laptop | 1 |
| Internet representation | Router | 1 |

## Device Functions

**Client (PC):** An end device that requests services or resources from other systems on a network.

**Server:** A computer that provides services, applications, or resources to clients.

**Switch:** Connects devices within a local area network and forwards Ethernet frames based on MAC addresses.

**Router:** Connects different IP networks and forwards packets between them based on routing information.

**Firewall:** Controls network traffic according to defined security policies.

**Attacker Laptop:** Represents a potential external threat source for future network security exercises.

## Network Topology

I designed the topology to represent two hypothetical branches: Kigali and Nairobi.

The Kigali branch contains two PCs connected to a switch, which connects to a router and firewall.

The Nairobi branch contains two servers connected to a switch, router, and firewall.

An additional router represents the Internet, while a laptop represents a potential external attacker.

### Topology Screenshot

![Network Topology](topology.png)

## Procedure

1. Opened Cisco Packet Tracer.
2. Added two Cisco 2911 routers.
3. Added two Cisco 2960 switches.
4. Added two Cisco ASA 5505 firewalls.
5. Added two PCs and two servers.
6. Added a router to represent the Internet.
7. Added a laptop to represent a potential external attacker.
8. Arranged the devices into two branches.
9. Connected the devices using the Automatically Choose Connection Type tool.
10. Saved the topology as a Packet Tracer project.

## Observations

- PCs and servers are end systems.
- Switches, routers, and firewalls are network infrastructure devices.
- Different networking devices perform different roles.
- Cisco Packet Tracer provides a simulated environment for creating network topologies.
- The topology represents a simplified multi-branch network.

## Scope and Limitations

I completed the device-identification and topology-construction requirements for this introductory lab. IP addressing, routing, firewall policies, and end-to-end connectivity testing were outside the assigned scope. The diagram is a topology deliverable, not a claim of a fully configured network.

## Lessons Learned

I gained hands-on experience selecting routers, switches, firewalls, servers, and client devices, arranging them into a two-branch network, and building the intended connections in Cisco Packet Tracer.

## Next Steps

Continue studying network fundamentals before progressing to device configuration, IP addressing, and connectivity testing.

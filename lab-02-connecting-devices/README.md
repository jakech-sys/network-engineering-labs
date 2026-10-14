# Lab 02 — Network Cabling and Physical Connectivity

## Objective

Identify appropriate network transmission media and connect devices in Cisco Packet Tracer while **assuming Auto MDI-X is unavailable**. This exercise develops foundational understanding of copper straight-through cables, copper crossover cables, multimode fiber, single-mode fiber, and distance-based media selection.

This is a **physical connectivity and media-selection lab**. Successful network-layer communication has not been established or claimed.

## Lab Environment

- **Tool:** Cisco Packet Tracer
- **Lab file:** `Day 02 Lab - Connecting Devices.pkt` (source file prepared; repository upload pending)
- **Evidence:** Topology screenshot (prepared; repository upload pending)
- **Topology:** Two groups of access switches and end devices connected through routers, with a longer-distance link between the upper routers

The diagram includes four labeled routers (R1–R4), eight switches (SW1–SW8), three PCs (PC1–PC3), and one server (SRV1). It also labels illustrative link distances of **50 m, 250 m, and 3 km**. These distances are exercise assumptions, not field measurements.

## Cable Selection Principles

### Copper Ethernet when Auto MDI-X is unavailable

| Connection | Traditional cable choice | Explanation |
| --- | --- | --- |
| PC to switch | Straight-through | Typical MDI to MDI-X connection |
| Server to switch | Straight-through | Typical MDI to MDI-X connection |
| Router Ethernet interface to switch | Straight-through | Typically MDI to MDI-X |
| Switch to switch | Crossover | Typically MDI-X to MDI-X |
| Router Ethernet interface to router Ethernet interface | Crossover | Typically MDI to MDI |

**Important qualification:** “Same devices use crossover; different devices use straight-through” is a useful beginner mnemonic, **not a universal rule**. The decisive factor is the Ethernet interface's MDI/MDI-X behavior. Many modern interfaces support Auto MDI-X, which automatically compensates for the wiring arrangement. Actual firewalls and other devices require checking their port types and documentation.

For common twisted-pair Ethernet installations, the usual structured-cabling **channel** limit is **100 m**, subject to the applicable Ethernet standard and cable specification.

### Optical fiber

| Illustrative link | Appropriate consideration | Qualification |
| --- | --- | --- |
| **50 m** | Copper Ethernet can be appropriate | Requires a supported copper interface and a properly specified cable |
| **250 m** | Multimode fiber may be appropriate | Validate fiber grade, speed, optical transceivers, and allowable link loss |
| **3 km** | Single-mode fiber is generally appropriate | Requires compatible single-mode optical interfaces and sufficient optical budget |

**550 m is not a general boundary between multimode and single-mode fiber.** Supported reach varies by Ethernet standard, data rate, fiber grade, transceiver, and optical power budget. Fiber media also require compatible interfaces/modules at both ends.

## Procedure

1. Opened the Day 02 exercise in Cisco Packet Tracer.
2. Reviewed the connected device types, interface relationships, and indicated link distances.
3. Applied traditional straight-through versus crossover selection rules while assuming Auto MDI-X was unavailable.
4. Considered multimode and single-mode fiber for the longer-distance links.
5. Examined the resulting connections in the logical topology.
6. Saved the Packet Tracer activity and captured a topology screenshot.

## Observations

- End devices, switches, and routers have different traditional Ethernet wiring requirements depending on interface type.
- Copper cabling is a practical option for local links within supported Ethernet distance limits.
- Fiber selection requires considering **both link distance and the physical-layer specifications**.
- The illustrative 3 km link motivates the use of single-mode optics; a 250 m link may support multimode optics when the chosen specifications permit.
- The screenshot is evidence of a designed topology and media choices, **not proof of working interfaces, correct configuration, or successful packet delivery**.

## Scope and Verification Status

| Activity | Status |
| --- | --- |
| Device topology reviewed | Completed |
| Physical-media selection studied | Completed |
| Cable type and distance reasoning documented | Completed |
| IP addressing and routing configuration | Not part of this lab |
| Interface status and link compatibility testing | Not independently verified |
| End-to-end ping and traffic verification | Not performed / not evidenced |

**Note:** Colored indicators in a Packet Tracer screenshot alone do not establish the cause of a down link. Device status, supported ports/modules, cabling, and interface configuration should be examined before diagnosing a failure.

## Lessons Learned

The correct physical connection is not determined solely by whether two devices are identical or different. Copper Ethernet cabling traditionally depends on interface pin assignments, while fiber links must satisfy distance, speed, connector, transceiver, and optical-budget requirements.

This activity reinforced why engineers verify hardware compatibility and physical-link behavior before troubleshooting IP addressing or routing.

## Next Steps

1. Inspect interface types and link status in Packet Tracer.
2. Document exact interfaces, cable choices, and any unsupported connections.
3. Configure IP addressing on a small, supported subset of the topology.
4. Verify connectivity with interface-status checks, ping tests, and documented results.
5. Publish reproducible configuration and validation evidence.

---

**Documentation standard:** This report describes the exercise and observed topology without claiming network operation that has not been demonstrated.

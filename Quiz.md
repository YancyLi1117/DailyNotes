# Quiz 1

[TOC]

## Review of Internet Technologies

### Control and Management on the Internet

Elementary Control Elements

- Addressing

- Neighbour Discovery:

  **Link Management Protocol (LMP)**: A prerequisite for network-wide link-state dissemination and topology discovery

- Topology Discovery: 

  The topology and resource state of the whole network can be determined by disseminating link-state update messages.

  Reactive versus Proactive dissemination

- Path Selection (route computation)

- Protection/Restoration

- Signalling

### Evolution of the Internet Technology

#### Packet-Switched Networks\-- 64 KB/sec

- Connectionless mode communication

  \- Sequence of the packets received may not be in order

  \- Traffic bottleneck due to the use of routing table

- IP routers with software-based routing core

  \- IP packets have a high error rate => large overhead on the error detection/correction in each intermediate node

- Use routing metrics and routing table in each node

#### Frame Relay-- Around 2 MB/sec

\- Released efforts in intermediate nodes\- Communication media is getting more reliable

Bandwidth bottleneck: - Variable length of frames => hardware cannot reach

#### Asynchronous Transfer Mode (ATM)-- 10Mbps to Gbps

Use a new protocol (PNNI) to handle control and management

\- High performance in switching data packets - Better mechanisms in traffic engineering

provision constant data rate using packet switching technique

### Industry Standardization Process

#### IP Over ATM (IPOA)

Used to connect IP and ATM networks

- dis : p22 Still bandwidth limitation - 10% cell tax

#### Multi-layer Switching

Alternatives to IPOA, but: \- Vendor-specific and not interoperable - Need a multi-vendor standard

#### Multi-Protocol Label Switching (MPLS)

- Independent and interoperable modules, including: P30
- **Functions of the MPLS**: Enhance routing functionality, Deliver new services swith ease

#### Virtual Private Networks (VPNs)

Private wide area networks by slicing the network resources for each subscriber

**LSR (Label Switched Router)**, **LSP (Layered Service Provider)**

- Design Issues: p36

### Software Defined Networking (SDN)

#### Problem

- Networks must keep up with exponential increases in traffic, and need more people and equipment to manage
- Networking is highly prescriptive, networks are consumed in intents. Few abstractions in traditional networking to hide details, which are exposed to and understood by consumers
- All elements are tightly coupled, and customers have little choice in selecting for specific uses.
- Network virtualization is nothing new, but today the engineers must manually translate high-level intents into low-level implementations.
- Optimal resource utilization is a challenge in networking 

Much easier to write, verify, maintain,...

- An interface for programming, understood by the end users
- **NOS(Network Operating System)** serves as a fundamental control block
- With a global view of the network, easy for optimal resource allocation

#### Interfaces

![1](https://i.postimg.cc/7YXzD7P8/655-1.jpg)

Driven by the emergence of **programmable transmissions and switching**

**ONF(OpenNetworking Foundation)** 

#### What can be achieved

- Simple but Intelligent and easily manageable service platform
- Heterogeneous and multi-vendor network control/management

## Wireless Communication Systems

### Infrastructure-based communication

#### Cellular Systems 

SDM (space division multiplexing): A geographic area is divided into smaller, circular areas called **cells**.

##### Advantages of smaller cells

- Higher capacity (SDM: frequency reuse) <-users 
- Less transmission power for MS (no BS problem) 
- Local interference only (MS<-->BS)
- Robust against failures of single components

##### Disadvantages of smaller cells

- Larger infrastructure (antennas, switches, ...) 
- Frequent handover
- Better planning: frequency assignment, etc.

#### Mobile Telecom Systems

##### 1G (1980’s)

- Voice signals are modulated (analogously) to 150MHz or upper and launched in the air
- **First mobile system** supporting international roaming and limited handover functions
- Replaced by 2G for digital transmission

##### 2G: Global System for Mobile Communications---GSM (1990’s)

- Goal---Phone + roaming in Europe

- Three services
  - bearer (data services)
  - tele (voice-oriented services with encrypted voice transmission and messages)
  - supplementary (A means of enriching user experiences, containing various enhancements for bearer and tele services )

- Architecture
  - **radio subsys (RSS)**: contains radio-specific entities: **BSS** (basic element in GSM, n BTSs correspond to 1 BSC (base station controller)), **BTS** (base transceiver station) and **MS** (User equipment and software for communications)
  - **network and switching subsys (NSS)**, the heart of GSM. Contains **MSC** (high-performance digital ISDN switches), **HLR**  (Home Location Register, most important database with all user relevant info.), and **VLR** (Visitor Location Register)
  - **operation subsys (OSS)**, 

- Voices are digitally encrypted

- Support SMS (short message services)

##### 2G+, Up to 54.7 (or 38.4) kbps

-  To enable data services on GSM
- HSCSD (High-Speed Circuit-Switched Data)
- GPRS (General packet radio service, 2.5G)

- EDGE (Enhanced Data rates for Global Evolution): not formally determined as 3G (2.9G)

<img src="https://i.postimg.cc/cJgCSrTd/655-2.jpg" alt="2" style="zoom:50%;" />

##### 3G---at least 200 kbps

- ITU 3GPP (3rd Generation Partnership Project) **defined 3G** 

  - Collaboration between a group of telecom standard assoc. 

  - based on evolved GSM spec. under IMT-2000 project

  - peak data rate of **at least 200 kbps**

  - dual mode with GSM (also called 3GSM) in handsets

- Based on ITU 3GPP

  \- UMTS (3GPP in EU, Japan, China)

   \- CDMA2000 (3GPP2 in US and Korea) - Reused almost all the network elements

- 3.5G HSPA on W-CDMA: - fast link adaptation and scheduling + fast HARQ
- 3.75G HSPA+: \- rate of 168Mbps by **MIMO（multi-input multi-output)**
- LTE (3GPP of ITU): Considered as **3.9G** since it does NOT match IMT-Advanced

##### 4G---100 Mbit/s for mobile, 1 Gbit/s for fixed users

- IMT-Advanced **defined by ITU-R in 2008 for true 4G** 

  - end-to-end all-IP network

  - take OFDMA-TDMA in the radio interface
  - 100 Mbit/s for mobile, 1 Gbit/s for fixed users

- LTE-Advanced---feature: p11
  - Backwards compatible: Works with GSM/GPRS/UMTS systems, Utilizes existing 2G and 3G spectrum and new spectrum, Low latencies, Supports handover and roaming to existing mobile networks, Reuse of existing sites and multi-vendor resourcing
  - Wide application: Both TDD and FDD modes, Large range of terminals, Mobility up to 350kph

##### 5G

- Key features

  \- Millimeter wave bands (26 - 60 GHz) for up to 20Gbps

  \- Massive MIMO (64-256 antennas) offers performance up to ten times than 4G-LTE

### Infrastructure-less communication
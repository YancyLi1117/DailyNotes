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
- **Functions of the MPLS**: Enhance routing functionality, Deliver new service swith ease

#### Virtual Private Networks (VPNs)

Private wide area networks by slicing the network resources for each subscriber

**LSR (Label Switched Router)**, **LSP (Layered Service Provider)**

- Design Issues: p36

### Software Defined Networking (SDN)

#### Problem

- Networks must keep up with exponential increases in traffic, need more people and equipments to manage
- Networking is highly prescriptive, networks are consumed in intents. Few abstractions in traditional networking to hide details, which are exposed to and understood by consumers
- All elements are tightly coupled, customers have little choice in selecting for specific uses.
- Network virtualization is nothing new, but today the engineers must manually translate high level intents into low level implementations.
- Optimal resource utilization is a challenge in networking 

Much easier to write,verify,maintain,...

- An interface for programming, understood by the end users
- **NOS(Network Operating System)** serves as fundamental control block
- With a global view of network, easy for optimal resource allocation

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

- **First mobile system supporting international roaming and limited handover functions**
- Replaced by 2G for digital transmission

##### 2G: Global System for Mobile Communications---GSM (1990’s)

- Phone + roaming in Europe

- Voices are digitally encrypted

  \- better rejection of noise

  \- FDMA (freq. division multiple access) and TDMA

- Support SMS (short message services)

##### 2G+, Up to 54.7 (or 38.4) kbps

-  To enable data services on GSM
- HSCSD (High Speed Circuit-Switched Data)
- GPRS (General packet radio service, 2.5G)

##### Toward 3G

- EDGE (Enhanced Data rates for Global Evolution)

### Infrastructure-less communication
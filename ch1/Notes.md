# Networking Notes Chapter 1

## Nuts and Bolts of the Internet
End systems are conneted together by a network of <b>communication links(wires/other)</b> and <b>packet switches</b>.

- <b>Transmission Rate of link</b> - Number of bits per second <b>(bps or bits/second)</b>

- <b>End systems or hosts</b> - Any device that uses the internet as a communication method.

Packets are used to send data through the links and packet switches.

## Packet switchers

- Help the packets reach their destination by selecting the most appropriate link from the packet switch's connecting links

- Must have multiple links attached to them to serve their purpose.

The sequence of communication links used by the packet to reach its destination is called a <b>route</b> or a <b>path</b>.

### Packet Switcher Types
Packet switchers can be in many shapes and flavors, but the two most prominent types in today's Internet are <b>routers</b> and <b>link-layer switches</b>

#### Routers
Typically in the network core.

#### Link-layer Switches
Typically used in access networks.

## Internet Service Providers (IPSs)
Internet Service Providers provide the network infrastructure for the internet. Each ISP has it's own network of packet switches and communication links. All ISPs must be interconnected (a part of the global network).

ISP Network Tiers:
- Lower Tier - Interconnected through <b>national and international upper-tier ISPs</b> such as Level 3 Communications, AT&T, Sprint, and NTT.
- Upper Tier - High-speed routers interconnected with high-speed fiber-optic links. 

Each ISP network is managed independently. Runs the IP protocol. 

## Protocols
Protocols control the sending and receiving of information within the Internet. The main protocols of the internet are <b>Transmission Control Protocol(TCP)</b> and <b>Internet Protocol(IP)</b>.

- <b>IP Protocol</b> - Specifies the format of the packets that are sent and received among routers and end systems.

The internet's principal protocols are known as <b>TCP/IP</b>.

<i>A <b>protocol</b> defines the format and the order of messages exchanged between two or more communicating entities, as well as the actions taken on the transmission and/or receipt of a message or other event.</i>

## Protocol Standards
Internet protocols must be standardised before they are widely used. <b>Internet Standards</b> are developed by the <b>Internet Engineering Task Force (IETF)</b>

The IETF standards documents are called <b>requests for comments (RFCs)</b>. RFCs define protocols such as TCP, IP, HTTP, and SMTP.

## How end systems communicate over the Internet
End systems attached to the Internet provide a <b>socket interface</b> that specifies how a program running on one end system asks the Internet infrastructure to deliver data to a specific destination program running on another end system.

A <b>socket interface</b> is a set of rules that the sending program must follow so t hat the Internet can deliver the data to the destination program. 

End systems or hosts can be divided into two categories:
 - <b>Clients</b> - PC's, smartphones etc.
 - <b>Servers</b> - Hosts that store and distribute web pages, stream video, relay e-mail etc.

 ## Clients
 Clients are usually PC's, mobile phones, etc.

 ## Servers
 Servers are poweful machines that store and distribute web pages, stream video, relay em-mail etc.

### Data Centres
The places where servers are located are called <b>data centres</b>. For example, Google has 50-100 data centres each with more than 100,000 servers.

## Access Network
The network that physically connects an end system to the first router (also known as <b>edge router</b>).

## Home Access: DSL, Cable, FTTH, Dial-Up, and Satelite
The two most commonly used types of broadband residential access are <b>digital subscriber line(DSL)</b> and <b>cable</b>.

### Digital Subscriber Line (DSL)
DSL uses a <b>DSL modem</b> to connect the end systems to the network with the <b>telephone line</b> (twisted copper wire) as a network link. At the end of the telephone line is a <b>digital subscriber line access multiplexer (DSLAM)</b> which listens for the DSL modem's high frequency tones (<b>analog signals/format</b>) and translates them into <b>digital format</b>. 

The telephone can carry data and telephone calls simultaneously by encoding it at different frequencies:

- A high-speed downstream channel, in the 50 kHz to 1MHz band
- A medium-speed upstream channel, in the 4 kHz to 50 kHz band
- An ordinary two-way telephone channel, in the 0 to 4 kHz band

On the customer side there is a <b>splitter</b> that separates the data and the telephone signals and forwards the data signals to the DSL modem.

On the Telco side DSLAM separates the data and phone signals and sends the data into the Internet.

DSL standard defines multiple transmission rates:
- 12 Mbps downstream and 1.8Mbps upstream [ITU 1999]
- 55 Mbps downstream and 15 Mbps upstream [ITU 2006]

When the downstream and upstream rates are different, the access is said to be <b>asymmetric access</b>.

Transmission rate can be limited from the Telco side. The distance to the CO, gauge of the twisted-pair line and degree of electrical interference can also have an impact on the transmission rate.

### Cable
Cable makes use of the cable television company's existing cable television infrastructure. There is a <b>fiber node</b> to neighbourhood-level junctions, from which <b>coaxial cable</b> is used to reach individual homes. A neighbourhood junction typically supports 500 to 5,000 homes. When both fiber and coaxial cables are used for the network, it is called <b>hybrid fiber coax (HFC)</b>

Cable internet access requires <b>cable modems</b>. From the ISP side there is <b>cable modem termination system (CMTS)</b> which converts analog signals from the cable modem to digital format.

DOCSIS 2.0 standard defines transmission rate downstream 42.8 Mbps and upstream up to 30.7 Mbps.

Important characteristic about cable Internet access is that it is a <b>shared broadcast medium</b>. Every packet sent by the head end (ISP side) travels downstream on every link to every home, and every packet sent by a home travels on the upstream channel to the head end.

### Fiber to the Home (FTTH)
Fiber to the home is an optical fiber path from the CO directly to the home. Commonly, these fiber paths are shared and are not for individual homes.

#### Passive optical network (PON)
Each home has an <b>optical network terminator (ONT)</b>, which is connected by dedicated optical fiber to a neighbourhood splitter. The splitter combines a number of homes onto a shared optical fiber, which connects to an <b>optical line terminator (OLT)</b> in the telco's CO. 

Packets coming from the OLT to the splitter are replicated by the splitter and sent to each ONT.

### Dial-Up
Obsolete

## Access in the Enterprise (and the Home): Ethernet and WiFi
Enterprises and sometimes homes use <b>local area network (LAN)</b> to connect an end system to the edge router. Ethernet is the most common access technology in corporate, university and home networks. 

Ethernet users use <b>twisted-pair copper wire</b> to connect to an <b>Ethernet switch</b> or a network of interconnected switches.

Ethernet users usually have 100 Mbps to 1 Gbps transmission rates, while servers usually have 1 Gbps to 10 Gbps access. 

Current ethernet technology can reach up to 400 Gbps for a single connection.

## Physical Media
The links between each transmitter-receiver pair that use electromagnetic waves or optical pulses are called <b>physical mediums</b>. Examples of physical media include twisted-pair copper wire, coaxial cable, multimode fiber-optic cable, terrestial radio spectrum, and satelite radio spctrum.

Physical media falls into two categories: 
- <b>Guided media</b> - Wwaves are guided along a solid medium, such as fiber-optic cable, a twisted pair copper wire, or coaxial cable 
- <b>Unguided media</b> - Waves propagate in the atmosphere and in outer space, such as in a wireless LAN or a digital satelite channel.

### Twisted-Pair Wire
Consists of two copper wires, each about 1mm thick, arranged in a regular spiral pattern. Wires are twisted to reduce electrical interference from similar pairs nearby. Typically, a number of pairs are bundled together in a cable by wrapping pairs in a protective shield. A wire pair constitutes a single communication link.

<b>Unshielded twisted pair (UTP)</b> is commonly used for computer networks within a building (LANs). Data rates for LANs using twisted pair range from 10 Mbps to 10 Gbps.

### Coaxial Cable
Consists of two copper conductors which are concentric rather than parallel. Coaxial cable can be used as a guided <b>shared medium</b>. Meaning each of the end-systems receives whatever is sent by the other systems.

### Fiber Optic
Can support up to hundreds of gigabits per second. Immune to electromagnetic interference, have very low signal attenuation up to 100 km, and are very hard to tap.

Higher cost of optical devices such as transmitters, receivers, and switches.

### Terrestrial Radio Channels
Characteristics highly depend on the propagation environment and the distance. Can be classified into three groups
- Those that operate over very short distance (one or two meters).
- Those that operate in local areas, typically spanning from ten to a few hundren meters.
- Those that operate in the wide area, spanning tens of kilometers.

### Satelite Radio Channels
A communication satelite links two or more Earth-based microwave transmitter/receivers, known as ground stations. The satelite receives transmissions on one frequency band, regenerates the signal using a repeater, and transmits signal on another frequency.

Two types of satelites are used in communications:
- <b>Geostationary satelites</b> - Permanently remain above the same spot on Earth. Placed to orbit 36,000 km above Earth's surface
- <b>Low-earth orbiting(LEO) satelites</b> - Placed much closer to Earth and do not remain permanently above on spot on Earth. They rotate around Earth (just like the Moon) and may communicate with each other as well as with ground stations.

## The Network Core
In network applications, end systems exchange <b>messages</b> with each other. For long messages, the sender breaks down the message into smaller chunks called <b>packets</b>.

If a packet is L bits and transmission rate is R bits/sec, then the time to transmit the packet is <b>L/R seconds</b>.

Question: Do packets get split up into smaller chunks equal to the transmission rate, or there is a mistake in the book?

### Store-and-Forward Transmission
Most packet switches use <b>store-and-forward</b> at the inputs to the links. Store-and-forward transmission means that the packet switch must receive the entire packet before it can begin to transmit the first bit of the packet onto the outbound link. 

- <b>L</b> - Packet size
- <b>R</b> - Transmission rate
- <b>L/R</b> - Time to send entire packet.

Time to send one packet = <b>L/R</b>

Time to send packet over N routers = <b>N * L/R</b>

Time to send P packets = <b>(P - 1) * L/R</b>

Time to send P packets over N routers = <b>(N + P - 1) * L/R</b>

### Queuing Delays and Packet Loss
Each packet switch has multiple links attached to it. For each attached link, the packet switch has an <b>output buffer</b> (also called <b>output queue</b>), which stores packets that the router is about to send to that link.

In addition to store-and-forward delays, packets suffer output buffer <b>queuing delays</b>. If the output buffer is full, the arriving packet will get dropped which is called <b>packet loss</b>.

### Forwarding Tables and Routing Protocols
Routers use a <b>forwarding table</b> to determine which link to send the packets to. The router matches the destination IP(or part of it) against the forwarding table.

The internet has a number of <b>routing protocols</b> that are used to automatically set the forwarding tables in routers.

This type of switching is called <b>packet switching</b>.

### Circuit Switching
There are two fundamental approaches to moving data through a network of links and switches: <b>circuit switching</b> and <b>packet switching</b>.

Circuit-switched networks <b>reserve the resources</b> (buffers, link transmission rate) needed to communicate between the end systems for the duration of the session.

When two hosts want to communicate, the network establishes a dedicated <b>end-to-end connection</b> between the hosts.

### Multiplexing in Circuit-Switched Networks
A circuit in a link is implemented with either: 
- <b>Frequency-division multiplexing (FDM)</b> - The frequency spectrum of a link is divided up among the connections established across the link. 
- <b>Time-division multiplexing (TDM)</b> - Time is divided into frames of fixed duration, and each frame is divided into a fixed number of time slots. When a network establishes a connection across a link, the network dedicates one time slot in every frame to this connection.

The width of the band is called <b>bandwidth</b>.

### Packet Switching Versus Circuit Switching
Packet switching makes more efficient use of resources, while circuit switching is more reliable (provides constant transmission rate).

Circuit switching is losing popularity to packet switching.

### Network of Networks
<b>Access ISPs</b> are ISPs that provide internet access to customers.

No ISP has presence in each and every city in the world. Instead, in any given region, there may be a <b>regional ISP</b> to which the access ISPs in the region connect. Each regional ISP then connects to <b>tier-1 ISPs</b>. Tier-1 ISPs are the largest ISPs and there are aproximately a dozen, including Level 3 Communications, AT&T, Sprint, and NTT.

A <b>point of presence (PoP)</b> is simply a group of one or more routers (at the same location) in the provider's network where customer ISPs can connect into the provider ISP.

Any ISP (except for tier-1) may choose to <b>multi-home</b>, that is, to connect to two or more provider ISPs.

To reduce the costs, a pair of nearby ISPs at the same level of the hierarchy can <b>peer</b>, that is, they can directly connect their networks together so that all the traffic between them passes over the direct connection rather than through upstream intermediaries.

A third-part company can create an <b>Internet Exchange Point (IXP)</b>, which is a meeting point where multiple ISPs can peer together.

<b>Content-provider networks</b> are private worldwide networks that are used by content-providers like Google. These networks can connect to tier-1 ISPs. 

## Delay, Loss, and Throughput in Packet-Switched Networks
The most important delays are:
- <b>Nodal processing delay</b>
- <b>Queuing delay</b>
- <b>Transmission delay</b>
- <b>Propagation delay</b>

Together, these delays accumulate to give a <b>total nodal delay</b>.

### Processing Delay
The time required to examine the packet's header and determine where to direct the packet is a part of the <b>processing delay</b>.

This delay can also include other factors, such as the time needed to check for bit-level errors in the packet that occured during transmission.

After this nodal processing, the router directs the packet to the queue that precedes the link to router B.

### Queuing Delay
At the queue, the packet experiences a <b>queuing delay</b> as it waits to be transmitted onto the link.

If the queue is empty, the queuing delay will be zero.

Queuing delays can be on the order of microseconds to miliseconds in practice.

### Transmission Delay
The <b>transmission delay</b> is L/R. This is the amount of time required to push (that is, transmit) all of the packet's bits into the link.

### Propagation Delay
Once a bit is pushed into the link, it needs to propagate to the next router. The time required to propagate from the beginning of the link to the next router is called <b>propagation delay</b>.

The bit propagates at the propagation speed of the link. The propagation speed depends on the physical medium of the link (that is, fiber optics, twisted-pair copper wire...) and it is in the range of:

2 * 10^8 meters/sec to 3 * 10^8 meters/sec

which is equal to, or little less than, the speed of light.

The propagation delay is the distance between the two routers divided by the propagation speed.

- Propagation delay = <b>d / s</b>

- <b>d</b> - Distance between routers
- <b>s</b> - Propagation speed of link

### Comparing Transmission and Propagation Delay
The <b>transmission delay</b> is the amount of time required for the router to push out the packet; it is a function of the packet's length and the transmission rate of the link, but has nothing to do with the distance between the two routers.

The <b>propagation delay</b>, on the other hand, is the time it takes a bit to propagate from one router to the next; it is a function of the distance between the two routers, but has nothing to do with the packet's length or transmission rate of the link.

<b>d_nodal = d_proc + d_queue + d_trans + d_prop</b>

### Queuing Delay and Packet Loss
If 10 packets arrive at an empty queue at the same time, the first packet transmitted will suffer no queuing delay, while the last packet transmitted will suffer relatively large queuing delay. (while it waits for the other nine packets to be transmitted).

<b>a</b> - average rate at which packets arrive at the queue

<b>traffic intensity</b> = (L * a) / R

If La/R > 1 then the average rate at which bits arrive at the queue exceeds the  rate at which the bits can be transmitted from the queue. Therfore, one of the golden rules in traffic engineering is: <i><b>Design your system so that the traffic intensity is no greater than 1.</b></i>

If the traffic intensity is less than 1, then only the nature of the arriving trafic impacts the queue delay. If more than 1 packets arrives every L/R seconds then there will still be queuing delay, but if packets come in periodically every (L/R)N seconds then there will not be any queuing delay.

In reality, packets arrive at random intervals.

#### Packet loss
When a packet arrives at a router with a full queue, the router <b>drops</b> the packet, and the packet is <b>lost</b>.

### End-to-End Delay
End-to-End delay is delay from source to destination through multiple routers. For this example, we will assume the queue delay is nelegable and network is uncongested.

- <b>d_proc</b> - Processing delay at each router
- <b>d_trans</b> - Transmission delay at each router = L/R
- <b>d_prop</b> - Propagation delay for each link

<b>d_end_to_end = N * (d_proc + d_trans + d_prop)</b>

# Glossary
- <b> Distributed Applications</b> - Any applications that communicate over the internet.

- <b>CO</b> - Central office
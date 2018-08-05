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


# Glossary
- <b> Distributed Applications</b> - Any applications that communicate over the internet.

- <b>CO</b> - Central office
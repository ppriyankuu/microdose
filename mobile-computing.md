## Mobile Computing
1. Explain the architecture of Mobile IP. How does it support seamless mobility across different networks?

#### Mobile IP Architecture:
Mobile IP is a protocol that allows mobile devices (called Mobile Nodes, MN) to move between different networks without changing their IP addresses. It ensures continuous internet connectivity by handling mobility at the network layer.

#### The architecture mainly involves three components:
- Mobile Node (MN): A device that moves across different networks while maintaining its original IP address.
- Home Agent (HA): A router on the mobile nodes's home network that maintains the node's location information and forwards packets to the mobile node when it is away from home.
- Foreign Agent (FA): A router on the visited network that provides routing services to the mobile node and communicates with the Home agent.

#### Working Mechanism:
    - When a mobile node moves to a new network, it registers with the foregin agent.
    - The FA then informs the home agent for the mobile node's new care-of-address (temporary address at the foreign network).
    - When someone sends data to the mobile node's permanent IP address, the HA intercepts the data and tunnels it to the care-of-address.
    - The FA recieves the tunneled packets and delivers them to the mobile node.

#### Support for Seamless Mobility:
Location Management: HA keeps track of the mobile node's current location.
Tunneling and Encapsulation: Data packets are encapsulated and forwarded through a tunnel to the current locaiton without the sender needing to know the node's movement.
Transparent Communication: the mobile node continues to use its permanent IP address, providing session continuity even when it moves across different networks.

2. Discuss the advantages and disadvantages of Ad hock networks.
#### Advantages
- Infrastructure-less: No need for a fixed information like routers or access points; nodes communicate directly.
- Cost-Effective: Since there is no need for central administration or wired infrastructure, setup costs are low.
- Self-configuring: Nodes automatically configure themselves, making deployment easy in emergencices like disaster recovery.
- Flexible and Scalable: Ad hoc networks can be easily scaled up or down depending on the number of participating devices.
- Robustness: Failer or a node does not necessarily result in network failure because the network can reorganise itself.
#### Disadvantages
- Limited Resources: Devices usually have limited battery power, processing, and memory.
- Security Challenges: Open medium and lack of centralized control make them vulnerable to attacks.
- Unstable Topology: Node mobility causes frequent route changes, making the network unstable.
- Lower Data Rates: Wireless links often provide lower data transfer rates compared to wired connections.
- Routing Overhead: Continuous updating of routes in a dynamic environment causes extra communication overhead.

3. What are the various types of wireless transmission media? Explain two with examples.
#### Types of Wireless Transmission Media:
1. Radio Waves
2. Microwaves
3. Infrared Waves
4. Bluetooth and Satellite Communication (special cases)

#### Radio Waves:
Radio waves are electromagnetic waves used for long-distance wireless communication.

They travel easily through walls and are widely used for radio broadcasting, Wi-Fi, and mobile phones.

Example: FM radio (88–108 MHz), Wi-Fi networks (2.4 GHz and 5 GHz bands).


#### Microwaves:
Microwaves have higher frequencies (1 GHz to 300 GHz) and are used for point-to-point communication.

They require a clear line of sight and are used in satellite links and cellular networks.

Example: Mobile phone communication (e.g., 4G, 5G), satellite TV.
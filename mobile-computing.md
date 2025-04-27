## Mobile Computing
1. Explain the architecture of Mobile IP. How does it support seamless mobility across different networks?

#### Mobile IP Architecture?
Mobile IP is a protocol that allows mobile devices (called Mobile Nodes, MN) to move between different networks without changing their IP addresses. It ensures continuous internet connectivity by handling mobility at the network layer.

The architecture mainly involves three components:
- Mobile Node (MN): A device that moves across different networks while maintaining its original IP address.
- Home Agent (HA): A router on the mobile nodes's home network that maintains the node's location information and forwards packets to the mobile node when it is away from home.
- Foreign Agent (FA): A router on the visited network that provides routing services to the mobile node and communicates with the Home agent.

Working Mechanism:
    - When a mobile node moves to a new network, it registers with the foregin agent.
    - The FA then informs the home agent for the mobile node's new care-of-address (temporary address at the foreign network).
    - When someone sends data to the mobile node's permanent IP address, the HA intercepts the data and tunnels it to the care-of-address.
    - The FA recieves the tunneled packets and delivers them to the mobile node.

Support for Seamless Mobility:
Location Management: HA keeps track of the mobile node's current location.
Tunneling and Encapsulation: Data packets are encapsulated and forwarded through a tunnel to the current locaiton without the sender needing to know the node's movement.
Transparent Communication: the mobile node continues to use its permanent IP address, providing session continuity even when it moves across different networks.
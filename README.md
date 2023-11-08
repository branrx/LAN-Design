# LAN-Design
Local Network Area design for a single building facilitating offices and laboratories across 3 floors.

##  PROBLEM DESCRIPTION
The client seeks to deploy a local area network (LAN) within a multi-story school building, catering to a collective of 120 users distributed across three floors. The specific challenge is to ensure that each sub-network is configured to support no more than 36 users while adhering to the cost constraints inherent in the utilization of a Class C network scheme.

### Constraints
- no more than 36 users per sub-network
- should accommodate 120 users
- low budget
- Class C IP address scheme
- sub-net mask of 255.255.255.224

##  NETWORK DESIGN OVERVIEW
In the network design, the primary constraint is the need to limit each sub-network to a maximum of 30 hosts while accommodating a total of 100 hosts across the network. To meet this requirement, it is necessary to employ more than four routers, as a network with only four routers would support a maximum of 120 hosts, falling short of the demand.

As a solution, a hierarchical structure is proposed. On the ground floor, Router 1 is deployed to manage up to 29 hosts and connects to Router 2 on the first floor. Router 2, in turn, connects to Router 3, also on the first floor. This configuration with two routers on the first floor accommodates the 46 devices, while adhering to the 30-host limit per sub-network.

On the second floor, Router 4 connects to Router 2, which acts as an intermediary, enabling connectivity between Router 1 and Router 4, and between Router 3 and Router 4. This design effectively supports a maximum of 120 hosts, aligning with the specified requirements and the 30-host constraint per sub-network.

Furthermore, this network design restricts each sub-network to a maximum of 29 hosts, complies with a Class C IP address scheme, and utilizes sub-netting techniques and a sub-net mask of 255.255.255.224 to allocate 32 host IP addresses per sub-network. To accommodate the 100 hosts, four sub-networks are created, each equipped with its own switch for host connections. Four routers are employed to establish connectivity between these sub-networks.

For validation and testing, the network's functionality and performance are assessed using CISCO Packet Tracer as a simulation tool. This ensures a thorough evaluation of the network's operational viability.

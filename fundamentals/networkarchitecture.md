# Network architectures

- A network can be designed in different ways. It could be a multi-layered network or could be a large network with just two layers.
- The architecture of a network depends on several factors, such as business requirements, the criticality of the functions running in the network, or even the cost factor. Sometimes a small organization might use a multi-layered network, while a large organization uses a two or three-layered network.

## Three-tiered Network

- Each network that is designed has a certain number of tiers. The three-tier network architecture is generally recommended specifically when you have a large amount of egress(outbound data) and ingress(incoming) data from a network. The three-tier architecture defines how the data flows in and out of the network.
- There are several advantages to a three-tier architecture. One of them is reduced latency because the data in transmission has to cross only three hops, which are the tiers. This eventually reduces latency compared to network architectures with more than three tiers. Other advantages are ease of management, scalability, performance, and ease of troubleshooting.
- The three tiers are Core, Distribution/Aggregation layer, and Access/Edge tiers. Each of the tiers is responsible for performing a specific function.

core tier:

- The Core tier is responsible for routing traffic in and out of a network. This tier consists of routers that connect a network to other networks or the Internet. They can be used to connect two geographically separated networks. You can also have switches at the Core layer, depending on how you have designed the network. The switches perform fast switching of packets that they receive.

distribution/aggregation layer:

- This is the second tier in the three-tiered network. It is responsible for implementing filtering using access control lists. The network policies are defined at this layer. At this layer, you implement Layer 3 switches to route packets within a network that consists of different subnets and virtual LANs (VLANs). At this layer, you can also implement different services, such as a firewall.

access/edge tier:

- In this tier, you will find the access switches that connect to the end clients, such as servers and systems. The packets routed from the Distribution Tier to this tier are further segregated and sent to the appropriate subnets or VLANs and then to the end clients. At this tier, the users are allowed access to the network services.

## Software defined networking

- Networks can be large and complex, and managing them can be highly difficult and time-consuming. SDN enables you to program complex networks for ease of management by implementing abstraction through different layers in a network. You can use specific applications to control and manage the networks without worrying about the technologies that are used to make up the network. In simpler words, it could be any underlying technology that runs the network. You can simply control the network with specific applications.
- To be able to manage and control the network, you need to program the network functionality and behavior. This is done through specific applications that use Application Programming Interfaces (APIs). One big advantage of SDN is openness, as it allows you to integrate technologies from different vendors and use them on the network without adding any complexity. SDN does not use the proprietary protocols from a specific vendor but rather uses open protocols.
- The SDN architecture contains four core layers:

Application Layer
At the application layer, you will find business applications that require the network and its services to work in a certain way. At this layer, you will find applications and network devices, such as load balancers and firewalls. It is the layer where applications and services, which define network behavior, reside. It communicates with the control layer through application programming interfaces (APIs).

Control Layer
In this layer, you will find the main SDN controller. This layer is considered to be the brain of the entire SDN. The controller in this layer is responsible for managing the network policies and traffic flow through the SDN.

Infrastructure Layer
The infrastructure layer, known as the data plane, consists of switches that handle the traffic. It works with the instructions provided by the control layer to handle the traffic.

Management plane
The management plane layer is responsible for network configuration, monitoring, and management. It works across all layers to ensure the smooth functioning of SDN

## spine and leaf

- The Spine and Leaf, a two-tier network architecture, comprises two layers known as spine and leaf. Because there are only two layers involved in this architecture, it offers an extremely high throughput and low latency. Other than this, it also offers high resiliency because of its use of the full-mesh topology.
- The `spine` is the backbone in the spine and leaf network, which contains the switches responsible for routing. These switches are high-end switches providing high-throughput and low latency. They can provide high-speed connections that can range from 40 to 300Gbps.
- Each `leaf` contains the switches that collect the traffic from connected servers and route it to the switches in the spine layer. Each leaf tree connects to all the switches in the spine layer using a full-mesh topology. Each switch in the leaf layer can work with 40, 100 or 300Gbps uplinks to the connected spine switches. It has dual connectivity - one with the device, such as a firewall or server, and another with the spine switch.

## Top-of-Rack Switching

- In the spine and leaf architecture, the switches are placed on top of the rack and connect with the devices and servers placed within the rack. These are the leaf switches that connect with the spine switches using a fiber optic cable. You can connect each server or the device to at least two leaf switches for redundancy purposes. The leaf switches connect to the spine switches using a full-mesh topology, which means that each leaf switch connects to every spine switch. As was discussed earlier, one spine switch does not connect with another spine switch in spine and leaf architecture. Similarly, the leaf switches do not connect with other leaf switches.

## Traffic flows

- In a network, the traffic flows from one end to the other end. Traffic may also flow into or out of the network to an external network, such as the Internet. There are designated names for traffic flows, which are essentially of two types:

East-West:

- Within a network or a data center, the traffic flows from one device to another device. For example, it could be a client connecting to a file server or switches exchanging information amongst themselves. This type of traffic is known as East-West traffic, which is horizontal.
- East-West traffic occurs on the same layer in a network. Organizations have started to reduce physical servers and use virtual infrastructure. The traffic from a virtual machine to a physical server is also considered East-West traffic.

North-South:

- North-South traffic moves vertically in a network, which means it flows in and out of the network or the data center. The edge devices, such as a firewall filter traffic coming into and going out of the network. The traffic that enters into a network is known as the southbound. Traffic going out of the network is known as northbound traffic.

## Branch Office vs. On-premises Datacenter vs. Colocation

- Many organizations have a smaller branch office. In most cases, the branch offices directly connect to the main office’s data center for file access or even authentication. Some organizations keep everything at their centralized data center, but others choose to use a distributed environment. There is no right or wrong method of choosing a specific method. It is driven by business requirements as well as cost.

branch office:

- In this scenario, the network is distributed. Some of the servers, such as authentication and file servers, are located at the branch office. This helps in saving bandwidth as well as ease of management of these servers. This approach works well if there are enough users in the branch office and one or more IT professionals are available to manage these servers. The branch offices are connected with the main office data center through WAN links in most cases. This method is also often used when there is no reliable connectivity between the branch offices and the main office. In such a scenario, it is better to offload the servers to the branch office to keep them functioning

On-premises:

- An organization maintains and keeps all servers in a centralized data center. The branch offices connect to the on-premise data center using high-speed and reliable connections, if there are any. The main office has the main on-premise data center that keeps all the servers in a centralized location.
- The key reason for using this approach is that the organization has centralized control of the logical and physical environment. The management and maintenance of the infrastructure are relatively easy than having them in a distributed environment.

colocation:

- An organization can also opt for the colocation approach. An organization may simply use a third-party location to host its servers and networking infrastructure. In this approach, only the physical space of the third party is used, but the organization maintains its hardware and software infrastructure. The reason for choosing this approach is to use skilled manpower and a secure environment with high bandwidth availability. Also, the organization saves on the physical location along with added costs, such as electricity. The organization pays a monthly fee depending on the services that it uses.

## Storage area networks

- A storage area network, known as SAN, is a collection of storage devices that form a network. The network of storage devices can communicate directly with each other as well as devices on other networks and can span over multiple sites of an organization. Unlike the Ethernet network, a SAN is a specialized storage network. It can also contain various components like: Servers, Switches, Storage devices.
- The default network transmission method used by SAN is Fibre Channel. When you configure a SAN on a network, it appears as a disk array that the users can connect to. You need to use a different server to manage SAN.
- Large organizations use SANs because they are: Extremely fast, Highly fault-tolerant, Capable of storing large volumes of data
- If one of the SAN devices fails, the data is retained and made available on other devices. A SAN can use one of the three connection types:

Fibre channel over internet(FCoE):

- FCoE is a transport layer protocol that encapsulates Fiber Channel frames over an existing Ethernet network. With FCoE, you can utilize the existing Ethernet with its equipment and leverage the high speed of the Fiber Channel.
- The servers in the data center are connected to the FCoE switches, which further connect to the SAN. The servers are still running on the Ethernet network but connect to the FCoE switches using the FCoE protocol.

fibre channel:

- Fibre Channel is a Transport layer protocol that connects a SAN to another network. Instead of using typical protocols like TCP or UDP, Fiber Channel provides high speed up to 5 Gbps. The speed of the transmission is not dependent on the client’s network. Fibre Channel can be implemented in different ways, such as:
- Point-to-point (FC-P2P): Works like peer-to-peer. Two devices directly connect to form a network. This type of implementation has limited connectivity and does not allow more than two devices to communicate.
- Arbitrated loop (FC-AL): Forms a token ring kind of network in which all devices are configured in a loop. Just like a token ring network, a single device failure brings down the SAN network.
- Switched fabric (FC-SW): Works more like an Ethernet network where all SAN devices are connected to the Fibre Channel switches.

Internet Small Computer Systems Interface (iSCSI):

- Internet Small Computer Systems Interface, commonly known as iSCSI, is a Transport layer protocol that works on top of the TCP protocol and uses it for fast data transmission, which may occur within a LAN, over the WAN, or the Internet. The benefit of using iSCSI is that it is inexpensive and can use the existing Ethernet network.
- All you need to do is install the iSCSI initiator on the client devices and send commands to the SAN devices. You can still use the same Ethernet switch to send these commands to the SAN devices.

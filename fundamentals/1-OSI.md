# OSI

- The OSI (Open System Interconnect) Model is a framework that is used to describe the `functionality and interoperability` of networking components. These networking components can consist of hardware or software.
- This model was used to `standardize networking protocols` allowing interoperability of different hardware and software vendors.
- in early days of networking communications if one company chooses a one network vendor they have to stick with that vendor and if any other company has any other network communication vendor they won't be able to communicate with each other
- the `open system interconnection model (osi)` brings a layered approach to the networking functions, so it allows us to standardize the network communications
- it is developed by the `international organization of standardization`
- it consist of `7 layers`, the top 3 layers are `application layer` things like encrytion, decrytion, session establishment happens at this layers and bottom 4 layers are `supporting network functionality`, when we are sending information through this layer from source to destination it shouldn't have to worry about the format or any syntax, some example are data transport addressing, routing, media access, electrical and mechanical characteristics.
- the data that exists we want to send on network is `not ready` to go on the network, so the upper layer help us to do that and when the data gets ready to transmit through network the lower layer `makes sure` that data gets transmitted from the source address to the destination address

## Application layer 7

- its main purpose is to give the application and the data to give access to the network
- The application layer is the top layer of the Open Systems Interconnection (OSI) model and is `the     only layer that directly interacts with user` data. It controls how applications communicate with other devices, and ensures that applications can communicate with other applications on different networks and computer systems
- This layer also makes a `request` to its bottom layer, which is presentation layer for receiving various types of information from it
- some of `protocol` of application layer are: DHCP, DNS, FTP, SMTP, HTTP, POP3.
- for more go [here](https://www.geeksforgeeks.org/application-layer-in-osi-model/)

## Presentation layer 6

- presentation is about the `format` of the data
- This layer is also known as `Translation layer`, as this layer serves as a data translator for the network
- some of the example of the presentation layer are: SSL, SSH, compression, encryption, decryption, encoding.

## Session layer 5

- this establishes, maintains and terminate session communication.

## Transport layer 4

- The Transport layer’s function is to deliver data across network connections. The most commonly used protocols are TCP (Transmission Control Protocol) and UDP (User Datagram Protocol). Different protocols will have different functionalities when transporting data across the network. For example, error checking is done using the TCP protocol.
- this is vehicle layer to make information go from one place to another.
- we have 2 choices for the transport protocols: `transmission control protocol(TCP), user datagram protocol(UDP)`. these are the 2 primary transport protocol we have today in our networks

## Network layer 3

- network layer is responsible for `routing`
- This layer is responsible for `forwarding` packets to specific routes on the network.
- This layer analyses the packets received and determines if it has `reached its destination` and then passes it to the Transport layer. If it is not the final destination, it will pass it to the Data link layer until it reaches its final destination.
- The Network layer is also responsible for `updating routing tables`.
- this is where routing protocols works at like: IP
- [more](https://www.geeksforgeeks.org/network-layer-services-packetizing-routing-and-forwarding/)

## Datalink layer 2

- The Data link layer provides communication between directly connected devices. It also provides error handling for the OSI model's physical layer. It consists of two sub-layers, Media Access Control (MAC) and the Logical Link Control (LLC) layers. Most `switches` operate on the Data link layer or Layer 2 for communication, but there are exceptions where switches can also work on Layer 3 and are referred to as a Layer 3 switch where `routing` capabilities are required.
- this layer is divided into 2 parts: `Logical link control(LLC), media access control(MAC)`
- [more](https://www.geeksforgeeks.org/data-link-layer/)

## Physical layer 1

- Ensures the physical communication between the devices and converts an electrical pulse to binary.
- It defines the specific standard to which the physical components must comply to. The most commonly used protocols include the following, IEEE.802.11, IEEE.802.3 and several others.

## Identifying components associated with layers 1 to 3 of the OSI model

- The first three layers of the OSI Model consist of the Physical, Data-Link and Network layers. The Physical Layer of the OSI Model is responsible for the communication between devices and deals with the physical connection to a network. After a connection has been established by the Physical layer, the Data-Link decapsulates the packets to form frames, which are passed to the Network layer. The frames received from the Data-Link layer are then sent to the Network Layer, which determines where the frames need to be sent to using the headers, which contain the routing information for these frames. The Network layer allows to move traffic to networks not directly attached.

Data link:

- components associated with the `data link layer` is drivers and MAC address. The network software driver facilitates the interaction between the hardware component and the Operating System and forms part of the Data-Link layer of the OSI Model.
- By executing the command `ipconfig /all` on window shell, the network configuration of the device is displayed. The device’s IP address is displayed, and the physical address is also displayed. A device's physical address is referred to as the MAC address. This is associated with the specific `Network Interface Card (NIC)`. A MAC address is a `unique hexadecimal combination` that is used to identify the NIC. Different hardware vendors have different combinations on how these MAC addresses are compiled.
- `arp -a` The Address Resolution Protocol (ARP) resolves IP addresses to MAC addresses. To facilitate network communication, an IP address needs to be assigned to the network adapter. The IP address is then allocated to the MAC address, ensuring communication to other network devices. A MAC Address functions on the Data-Link layer of the OSI model.

network layer:

- The network components that are associated with the Network Layer of the OSI Model consists of the following: `IP address, Subnet mask, Default Gateway, Routing information`
- The Network layer inspects the headers of the packet received from the Data-Link layer to determine if it has reached its final destination. If not, it will forward the packet to the correct destination.
- From the output of the command `ipconfig /all`, the IP address, Subnet mask and Default Gateway is displayed. These are core components of the Network layer.
- The route add command `route -p add 'ipaddress' mask 'subnet' 'gateway'` creates a persistent route to the different subnets enabling communication across different subnets through the router.
- The `ping` command is used to verify that the newly assigned IP address can communicate with another device on a different subnet.

## Identifying Components Belonging to Layers 4 to 7 of the OSI Model

- OSI model layers 4 to 7 comprise the Transport, Session, Presentation and Application layers.

Identify Components of the Transport Layer of the OSI Model:

- Several different protocols operate on the Transport Layer of the OSI Model. These include TCP (Transmission Control Protocol) and UDP (User Datagram Protocol).
- 

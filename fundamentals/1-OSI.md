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

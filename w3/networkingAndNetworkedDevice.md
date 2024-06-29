# Networking and Networked device

- `network devices` are those devices with which we actually made up a infrastructure of a network, they help to move data to wherever its going
- `networked devices` are those devices that uses that network for their functions
- There are several networking devices that are an essential part of a network. They are the `core part` of a network without which you may not have a complete network. For example, without a switch or a router, it is difficult to form a network and connect it to the Internet. They help in routing, forwarding, managing, or filtering network traffic. For example, a firewall filters incoming and outgoing traffic. These devices help other dependent devices, such as a printer, to function on the network.

## networking devices

Hub:

- A hub is a network device that has several ports that connect end devices to the network.
- A hub is used to connect systems and other devices and allow them to communicate with each other. Any information received on one of its ports from an end device is repeated and transmitted to all its remaining ports without regard to any addressing present in the frame header. This is because a hub does not have any routing tables and sends the information to all available ports.
- It is considered to be a device without intelligence and cannot be assigned an IP address.

layer 2 switch:

- A network switch is a device that can connect several systems or devices to a network. It performs several tasks, such as, send and receive data to the destination device. It is similar to a hub but has key differences
- Recognizing frames
- Knowing the source and destination MAC addresses of the incoming frame along with the port on which it was received
- Sending the frames directly to the correct port
- Ability to send the frames to all other ports except the one on which it was received if it cannot figure out the destination of the frame
- Uses MAC addresses to send frames
- On Ethernet networks, the device uses MAC addresses to send frames to the appropriate ports. A switch will maintain a MAC address table that maps MAC addresses to ports. If a destination MAC is not in the MAC table, the switch will broadcast the frame out to all its ports except the port on which the frame was received.
layer 3 switch:

- A layer 3 switch is also known as a multilayer switch. It is essentially a switch that can perform basic Layer 3 (Network Layer of the OSI model) functions such as static routing, dynamic routing and access-list implementation. It can perform ``inter-VLAN routing`, allowing communication between the VLANs configured within it.
- One of the key advantages of a Layer 3 switch is that it can act like a Layer 2 switch and a router. As a Layer 2 switch, it can simply forward frames. When working as a router, it can forward frames to different subnets of a network.

Routers:

- A router, as the name suggests, is a device for routing packets on a network.
- A router is typically installed on the edge of the network to send and receive data from the system residing on the Internet. 
- Using a router, you can connect several network segments. A classic example of different network segments can be the Internet. Different network segments are present on the Internet, but the traffic is routed through the routers, making intelligent decisions to route the traffic to a specific destination.
- A router is inherently a Layer 3 device and routes traffic based on IP addresses. Other functionalities of a router include implementing access lists, dynamic routing protocols, and `Network Address Translation (NAT)`.

access point:

- An access point, more commonly known as the wireless access point, allows users to connect to a network wirelessly without using a cable for each user. The access point itself would require a single cable through which both data and power can be provided. A single access point in each room with an uplink to a central switch would suffice for the needs of the network, thus minimizing the amount of cabling installed. An access point, depending on the configuration, can also be connected to a wired network.
- An access point comes in handy when you have mobile users in your office. If you have a wired network, the users are limited to specific locations. An access point can transmit signals only to a specific distance. If users move away from that distance, they do not get the signals. For example, if an access point can transmit signals to 100 meters, as the user starts to move away from the access point, the signals start to degrade. If the user moves out of the 100-meter range, then the signals are lost. In a way, you can think of an access point as a switch or a hub, which allows several users to connect their devices.

wireless LAN controller (WLC):

- In an office environment, there can be several wireless access points. You need to manage them individually. Each of these wireless access points works independently and cannot communicate with each other. From an administrative point of view, this can be quite challenging. Managing one or two can still be easy, but if 20-25 of them are deployed, individually managing them can be a time-consuming task.
- With a Wireless LAN Controller (WLC), you can manage the deployed wireless access points. WLC becomes the central management authority for all existing wireless access points. All wireless access points are centrally controlled, managed, and maintained.
- With a Wireless LAN Controller (WLC), you can manage the deployed wireless access points. WLC becomes the central management authority for all existing wireless access points. All wireless access points are centrally controlled, managed, and maintained.
- some of the benefits are:
- Centralized management
- Flexible deployment of wireless access points
- Simplified wireless network maintenance
- Interference detection
- Wireless access point status detection
- `repeaters`
- `load balancers`
- `proxy servers`
- `voice gateway`
- `firewall`
- `VPN headend`
- `media converters`

## networked devices

- `network printers`
- `VoIP phone`
- `IP cameras`
- `HVAC controller and sensors`
- `SCADA`
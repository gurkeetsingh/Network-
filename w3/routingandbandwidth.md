# Routing and bandwidth

- routing is very important because it allows us to communicate off our local area network or it allows us to communicate across networks
- routing is deciding a `best` route from source to destination
- `static routing`
- `time to live (TTL)`

## Routing protocol configuration

- The Routing process is performed on layer 3 devices, such as a router, firewall and a layer 3 switch. It involves forwarding packets from the source to the destination.
- The routing process is performed based on the destination IP address (or other factors in the case of policy-based routing).
- The L3 device uses its routing table to decide and choose the best path to the destination. The routing table is populated either through static routing or dynamic routing protocols like RIP, OSPF and similar.

## steps to configure static routing

1. open the router interface
2. enable (to enter the exec mode)
3. configure terminal (to the enter the configuration mode)
4. hostname NYEDGE1 (to add a hostname)
5. interface GigabitEthernet 0/1 (to enter the interface configuration mode, a router interface is a physical connection point between a router and devices)
6. ip address 10.10.0.1 255.255.255.252 (to assign an IP address and enable the interface)
7. end (to get out of configuration mode)
8. ping 10.10.0.2 (to check the basic connection between the devices)
9. show ip route (is used to view the routing table of the router)

- ip route 192.168.100.0 255.255.255.0 10.10.0.1 (in this we are setting a static route with a next hope at a 10.10.0.1 address)
- 192.168.100.0/24 is used as the destination network and 10.10.0.1 as the next hop. Instead of the whole subnet, 192.168.100.1/32 can be used as the destination, and a static route can be created to `just this host`.
- to delete a static ip use this command `no ip route --`

## default route

1. configure terminal
2. ip route 0.0.0.0 0.0.0.0 10.10.0.2 (this is used to create a default route with all 0 on ip address and subnet mask and the third address is of the router which is going to be the next hop on a network)
3. The Default route is specified as all 0’s.

## dynamic routing protocols

- In large organizations with several devices and networks, it is not practical to use static routing for connectivity. Instead, one or more of the dynamic routing protocols can be used. Dynamic routing enables routers (or layer 3 devices) to exchange routing information dynamically. After which, every device will select the best path to the destination and will include the route in its routing table.
- The most common dynamic routing protocols are RIP (Routing Information Base), OSPF (Open Short Path First) and BGP (Border Gateway Protocol). Another protocol that is used when the Cisco routers are configured is EIGRP (Enhanced Interior Gateway Routing Protocol).
- Dynamic routing protocol can be divided into three categories: Link state routing protocol, Distance vector routing protocol, Hybrid
- The `distance vector routing protocol` exchanges the whole routing table and chooses the best path based on distance, which is usually the number of hops. It could also use metrics such as delay, packet loss and similar. RIP is a distance vector routing protocol.
- the `link state routing protocol` sends information about all connected networks to all routers in the network. All routers will have the same information in their link state database and will calculate the shortest path to the destination. That particular route will then be installed in the routing table. OSPF is an example of a link state routing protocol.
- [routing protocols](https://community.cisco.com/t5/networking-knowledge-base/dynamic-routing-protocols-ospf-eigrp-ripv2-is-is-bgp/ta-p/4511577)
- `distance vector` in this a route is choosed in which there is a less router(hops) to make to get to a destination from the sender

## configure RIP

- RIP (Routing Information Base) is a distance vector routing protocol that uses the number of hops as a metric.
- The route with the lowest hops is considered the best route and will be included in the routing table
- Hop count is a number from 1 to 15, while 16 is considered an unreachable destination.
- There are two versions of the RIP protocol, version 1 and version 2. Version 2 is newer and supports classful networks and VLSM (variable-length subnet masking).

1. configure terminal
2. router rip
3. version 2
4. network (ip address to which you want to connect)
5. no router rip (to remove the rip)

## configure EIGRP (Enhanced Interior Gateway Routing Protocol)

- EIGRP (Enhanced Interior Gateway Routing Protocol) was created by Cisco.
- It is a hybrid protocol that has similar features to RIP and OSPF. It initially sends Hello messages to establish a neighborship between routers (like OSPF). Then it exchanges routing information and includes them in the topology table.
- The best route will be included in the routing table based on metrics such as bandwidth, delay load, and reliability. The route with the lower metric is considered to be the better route.

## configuring OSPF(open shortest path first)

- OSPF (Open Shortest Path First) is a link-state routing protocol. Unlike distance vector routing protocol, link state protocols exchange network information contained in the link-state database - LSDB. LSDB is exchanged using link state advertisement - LSA. Every router will build a link-state database that describes the network topology of the area. After exchanging LSA messages, every router runs the SPF (shortest path first) algorithm and chooses the best route to every destination and populates its routing table with those routes.

OSPF can be divided into sub-domains called areas, which is a logical collection of networks. Multiple areas are used in large environments to divide networks and limit the scope of route information distribution.
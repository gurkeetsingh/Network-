# IP addressing scheme

- Network devices need to be allocated an IP address to be able to communicate with other devices on the network. Different types of IP addresses are available to ensure communication.
- There are two important types for an IP addressing scheme, which are public and private IP addresses. Private IP addresses are used for internal communication in the network, while public IP addresses are used for external communication.
- Two different methods can be used to assign an IP address to a device. A static or dynamic IP address allocation. Static IP addresses need to be manually assigned by the Network Administrator, whereas a dynamic IP address is automatically assigned by a Dynamic Host Configuration Protocol (DHCP) server.
- IPv4 address is a 32 bit binary number
- it is reported in a `dotted decimal notation` with a subnet mask
- subnet mask shows us in binary that what portion of those 32 bits is going to represent our network id and portion is going to represent the host id
- ip address is made up of 3 parts: network id, node id(host id) and subnet mask
- subnetting is essentially is a binary division
- in ip address the lowest address is the network address and the highest address is the broadcast address and all the address in between is called hosts

private ip address:

- Private IP addresses are used for network communication on the internal network.
- These IP addresses are normally an IPv4 IP address and are referred to as an RFC1918 IP address
- Internal or private IP addresses are not reachable by external devices over the internet
- These IP address ranges can be used on multiple networks, ensuring that they are not reachable through the internet. A Network Address Translation (NAT) server is used to facilitate communication externally. The NAT server can either be a router or a firewall which will translate the private IP address to a public IP address to ensure external communication is possible. NAT server will only have a limited number of public IP addresses assigned to it, which minimizes the use of these public IP addresses
- Another implementation to reduce the use of public IP addresses is the use of Port Address Translation (PAT). Multiple devices can connect to the internet using only one public IP address for communication. PAT is used by routers to facilitate communication.

## IPv4 and IPv6 addressing solution

- The key difference between IPv4 and IPv6 is that IPv4 addresses are made up of a 32-bit numerical number grouped in 4 octets, whereas the IPv6 addresses are made up of 128-bit hexadecimal configuration grouped in 8 octets.
- IPv4 Public address: 104.95.181.163
- IPv6 Public address: 2a02:26f0:a1:685:0000:356e

Extended unique identifier (EUI-64):

- The unique IP address is generated without the need for a DHCP server or through manual assignment
- These types of addresses are generated by the host using the MAC address of the Network Interface Card (NIC). A MAC Address is a 48-bit hexadecimal number unique to the NIC.
- The host utilizes the MAC address by dividing it into two 24-bit parts and adding the 16-bit value of 0xFFFE in between to create the unique IPv6 IP address. This is also known as `Stateless Address Autoconfiguration (SLAAC)`.
- this is how a ip address is generated from mac address of the device:
    1. mac address- 12:11:5f:ac:7b:77
    2. IPv6 address- 12:11:5f:ff:fe:ac:7b:77

## subnet

- a subnet is a logical subdivision of an ip network. the process of dividing a network into two or more networks is called subnetting

steps to get a subnet mask:

1. convert the ip address from decimal to the binary form.
2. determine how many host id bits to become a network id bits. for 4 networks we need to change 2 bits of the host id. because the 2 bits have 4 different combinations

## Default gateway

- A default gateway is used by internal network devices to communicate to externally located network devices or resources. For example, when a user tries to connect to an external website, the request to access the website will be sent to the default gateway. The response from the website will then be passed to the default gateway directing the traffic to the device that requested it. Depending on the network configuration, a default gateway address can either be an IPv4 or an IPv6 IP address.

## virtual IP (VIP)

- A Virtual IP address (VIP) is not assigned to specific physical network adapters. VIP can be assigned to multiple servers or domain names. For example, if a company hosts a website, a VIP can be assigned to the cluster of web servers. Instead of being dependent on physical adapters, the network traffic is distributed through the VIP to an available physical network adapter. This increases the availability and redundancy of the network.
# Load balancing and NIC teaming

- To ensure that resources are highly available on the network, additional configurations can be done to ensure high availability and disaster recovery in the event of a device outage or failure. These configurations can include configuring Network Interface Card (NIC) teaming and Network Load Balancing.
- `Network Load Balancing` can be configured by adding an additional server with the same role installed to ensure that if the primary server fails, a failover can occur for high availability. For example, the Internet Information Services role can be installed on both servers to create a failover for an internal website.
- `Network Interface Card teaming` is configured by adding an additional network card to the device. The additional NIC can then be configured to share the network traffic for the device, ensuring high availability.
- A further configuration that can be made to ensure resources are highly available in the event of a disaster is to `configure multipathing`. In essence, different network routes to the same resource are configured, ensuring the resource is available if a network device becomes unresponsive.
- 
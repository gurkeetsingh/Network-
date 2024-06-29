# DHCP

- Dynamic Host Configuration Protocol (DHCP) is used on an internal network to dynamically distribute IP addresses to hosts on the network. By dynamically assigning IP addresses, it reduces the administrative effort for medium and large networks.

## DNS

- Domain Name Systems (DNS) is the heart of the network, and these systems translate hostnames to IP addresses on the network. For example, DNS is used to browse websites on the internet using easily remembered hostname like www.google.co.uk instead of using the IP address 216.58.210.195. Several different DNS servers exist, and most internal networks will have an internal DNS that can be used to translate the IP addresses to hostnames. These internal DNS servers will then communicate the internal requests to external DNS servers on the internet to resolve these internal requests.
- When a DNS server is configured, depending on the need, additional DNS server and functionality can be configured for the hierarchy of the network these include the following:
- Root DNS Servers: Root DNS servers' essential functionality is the translation of hostnames to IP addresses and provides answers to queries from devices on the network.
- Internal & External DNS Servers: An internal DNS server will be hosted inside of the network and will only be accessible for internally connected devices. An external DNS server can be configured on the same network and handle only external requests. If an internal DNS server gets a request from an internal device and can not resolve it, the internal DNS server will contact the external DNS server to resolve the specific request.
- Authoritative name servers: Authorative name servers contain specific information of the domain where it is located and are normally the last point of contact to resolve an IP address to a hostname.
- DNS caching & Time to live configuration: DNS caching is a temporary database stored on a client machine. This database contains records of the recently visited sites and resources by the user. Time to live (TTL) is the time specified for how long a specific record should be stored on a server before it will be removed.
- Recursive lookup: Recursive DNS queries are used when a DNS server queries other DNS servers on the network to determine the location of a specific IP address of a resource on the network.

Record type:

- The different record types can be configured on a DNS server to facilitate communication and access to resources located on the network. These records include the following:
- Canonical name (CNAME): CNAME records are used in conjunction with A records in a DNS system and are configured to point to the domain and never to an IP address. It can be used to set up aliases for resources on the network.
- Mail Exchange Record (MX record): MX records are configured on a DNS server to specify an SMTP server for the specific domain. These records are used to route outgoing emails to a mail server.
- Start of Authority (SOA): These records are part of the DNS Zone file and specify the Authoritative Name Server for the DNS zone. The details for the domain administrator and how often the DNS information needs to be updated are also part of these records.
- Pointer record (PTR): A PTR record provides the IP address associated with a domain name. It does the exact opposite of an A record.
- Text record (TXT): A domain administrator will create TXT records to add notes to the DNS system for reference. In addition, these records can also contain data referencing other devices.
- Service record (SRV): An SRV record is configured to point to a specific host and port on which the resource is available, for example, instant messaging or voice-over IP services.
- Name Server record (NS): Name Server records are configured to indicate which DNS server is authoritative in the domain. It provides information on the domain’s IP address.
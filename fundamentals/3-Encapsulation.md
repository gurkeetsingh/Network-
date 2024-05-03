# Encapsulation

- Data encapsulation and decapsulation is the process of adding or removing headers to the data that traverses across the network. This process ensures that the different layers of the OSI model can `communicate` with each other.
- it also adds `security and reliability` to the transmission of the data.
- Data that is sent across the network is encapsulated and decapsulated on `every level` of the OSI model. This is to ensure that each layer can communicate with each other.
- in this each layer depends on the lower layer for its services
- lower layer provide upper layers services.
- each layer provide additional information
- Encapsulation is a networking concept that adds information to a packet as it travels to its destination.
- The information has been added on the sender’s side, from the Application layer to the Physical layer.
- The data between the packet's header and trailer is called the `payload`. The header is the beginning of the packet, and the trailer is the end.
- `header` is the additional information that is given by each service
- when we are sending data we are `encapsulating` that data and when we are receiving that data as a destination  we are `decapsulating` it on the receivers device
- top to bottom is encapsulation and bottom to top is decapsulation in networking model(TCP/IP, OSI)
- network cares more about what is in headers than the data or payload itself.
- `Maximum tranmission unit(MTU)` describes the overall size and length of the entire encapsulated frame. this the maximum size that we transmit across the internet. if the size is more than the MTU the `ethernet` will discard it and you have to resend the information. this happens at `data link` layer

steps for encapsulation are:

1. The combined Application, Presentation, and Session layers of the OSI model utilizes the data from the application in the form of data streams and sends it to the Transport layer. Depending on the specific application, a header will be added to the data.
2. The OSI model's Transport layer receives the data from the top layers and divides it into smaller pieces referred to as `data segments`. The data is encapsulated by adding the correct header to each segment of the data. Each data header contains `sequencing information` to ensure that it can be `assembled` at the receiver.
3. In the next step for the data encapsulation process, the Network layer receives the data from the Transport layer and encapsulates it further by adding an additional header to each segment. These data headers `contain all the routing information to ensure delivery`. The data pieces are now referred to as a `data packet or datagram`.
4. After receiving the Network layer's data packet, the Data-link layer adds additional `headers and footers` to the datagram. These headers and footers `contain switching information and data relating` to the appropriate hardware components. The footer contains information about `error detection and control`.
5. In the final step, the Physical layer receives the data frames from the Data-link layer and encapsulates them by converting them to the `correct transport media` associated with the physical connections, for example, Ethernet or fiber mediums

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

## Decapsulation

- Data decapsulation is the process of converting data that was sent from another device by reversing the steps of data encapsulation. In other words, the process of data decapsulation will start at the Physical layer of the OSI model and end at the Application layer.

steps for decapsulation are:

1. The Physical Layer in the OSI model receives the encapsulated data from the sender and de-encapsulates it to the form of a data frame, which will be forwarded to the Data Link Layer.
2. The Data Link Layer receives the data from the Physical layer, de-encapsulates the data frames, and verifies if it has been sent to the correct destination. If an incorrect destination has been stipulated, the data frame will be discarded; otherwise, the footer of the data frame will be checked. If an error in the data is detected, it will request resubmission of the data frame. The de-encapsulated data frame is then sent to the Network layer.
3. The data frames from the Data link layer are passed to the OSI Model Network Layer, which is de-encapsulated. The packet header is checked to verify if the packet has been routed to the correct destination. If an incorrect destination is stipulated, the packet will be discarded; else, the packet is forwarded to the Transport Layer.
4. The Transport Layer receives the data frames from the Network Layer and de-encapsulates them. The first segment header is checked and verified, and then the data frames are assembled, which are then passed to the Application Layer.
5. The Application, Presentation and Session Layers receive the encapsulated data from the Transport Layer and de-encapsulates it. The application-specific data is then forwarded to the correct application, for example, a web browser.

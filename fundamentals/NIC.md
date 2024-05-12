# Network interface card(NIC), layer 2

- The network must provide a mechanism that gives each system a `unique identifier`—like a telephone number—so data is delivered to the right system. That’s one of the NIC’s most important jobs. Inside every NIC, burned onto some type of ROM chip, is `special firmware containing a unique identifier` with a `48-bit` value called the media access control address, or `MAC address`
- No two NICs ever share the same MAC address—ever. Any company that makes NICs must contact the Institute of Electrical and Electronics Engineers (IEEE) and request a block of MAC addresses, which the company then burns into the ROMs on its NICs.
- MAC address are always written in hexadecimal form. so it takes 12 hexadecimal numbers as each hexadecimal is made up of 4 bits. so `MAC address is made up of 48 bits`

syntax of MAC address:

- a MAC adrress is represented in this format: 00–40–05–60–7D–49. 6 groups of 2 hexadecimal numbers
- The first six digits, in this example 00–40–05, represent the number of the `NIC manufacturer`. Once the IEEE issues those six hex digits to a manufacturer—referred to as the `Organizationally Unique Identifier (OUI)`—no other manufacturer may use them.
- The last six digits, in this example 60–7D–49, are the `manufacturer’s unique serial number` for that NIC; this portion of the MAC is often referred to as the `device ID`
- All networks transmit data by breaking whatever is moving across the Physical layer (such as files, print jobs, Web pages, and so forth) into discrete chunks called `frames`. A frame is basically a `container` for a chunk of data moving across a network. A frame encapsulates—puts a wrapper around—information and data for easier transmission. The `NIC creates and sends, as well as receives and reads, these frames`

- Different frame types are used in different networks. All NICs on the same network must use the same frame type, or they will not be able to communicate with other NICs
- You can think of a frame in a different way as having three sections. The header (MAC addresses of reciever and sender and Type) starts, followed by the payload or data (whatever is encapsulated in the frame); this is followed by the trailer (the FCS) `frame check sequence`
- The FCS uses a type of binary math called a `cyclic redundancy check (CRC)` that the receiving NIC uses to verify that the data arrived intact
- the frames can hold at most `1500 bytes of data used in ethernet`. so the software on the upper layer chop the data into the frame size which is then handover to the NIC for sending. on the receiver side software combines the data coming from sender in a correct sequence

## two jobs of NIC

- Consider how data moves in and out of a NIC. On one end, frames move into and out of the NIC’s network cable connection. On the other end, data moves back and forth between the NIC and the network operating system software. these are broken down into 2 distinct jobs
- The first job is called the `Logical Link Control (LLC)`. The LLC is the aspect of the NIC that talks to the system’s operating system (usually via device drivers). The LLC handles multiple network protocols and provides flow control.
- The second job is called the `Media Access Control (MAC)`, which creates and addresses the frame. It adds the NIC’s own MAC address and attaches MAC addresses to the frames. each frame the NIC creates must include both the sender’s and recipient’s MAC addresses. The MAC sublayer adds or checks the FCS. The MAC also ensures that the frames, now complete with their MAC addresses, are then sent along the network cabling

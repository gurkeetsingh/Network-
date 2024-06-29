# cable and connection

- In computer networking, different kinds of network cables are used based on different requirements. Cables are used to transmit information either electronically or in the form of light.

## copper twisted pair cable

- in this we have a 8 twisted conductors. there are 4 pair of twisted cabling in this
- the twist within the cables help them to strenthen the cables resiliency to electromagnetic interference
- Twisting the cables reduces noise (crosstalk). When the electrical signal passes through each copper wire, a magnetic field is created around each wire as well. This magnetic field can create noise, but when the cables are placed close to each other, the magnetic fields are opposite to each other, and they cancel each other out.
- in the `shield twisted pair` the only difference is that the twisted pair of cable are wrapped around by a `foil shielding` to make it more reliable against the electromagnetic interference
- the `outer jack` is the outer part of the cable it is of different types: `plenum and non-plenum`
- non-plenum is the average outer jack cable which is used commonly it also known as `polyvinyl chloride(PVC)` and the other one is plenum cable, this is rated for HVAC(heated ventilation and air conditioning) and is more expensive than non-plenum.

TIA/EIA twisted pair categories:

- CAT here means category
- CAT3, application= ethernet, 10Mbps, distance= 100m
- CAT4, token ring, 16Mbps, 100m
- CAT5, fast ethernet, 100Mbps, 100m
- CAT5e(enhanced), gigabit ethernet, 1Gbps, 100m
- CAT6, gigabit ethernet, 1Gbps(10Gbps), 100m(55m)
- CAT6a(augmented), gigabit ethernet, 1 and 10Gbps, 100m
- CAT7(iso not tia), gigabit ethernet, 1 and 10Gbps, 100m

## coaxial cabling/ RG 6

- in this we have a single copper cable or conductor in the middle and have braided shielding around it
- In a Coaxial cable, a copper conductor, which is the inner part of the cable, is surrounded by a metallic foil or braid. This foil helps to reduce noise and interference. The copper cable and the metallic braid are insulated by a cable jacket. A coaxial cable supports speed with 10 Mbps to 100 Mbps range. It is more expensive than a twisted pair cable. One of the advantages it offers against twisted pair cable is that it can have a maximum segment length of up to 500m. Primary application of coaxial cables is residential TVs. Other than that, it can be used for satellite transmission and Internet services, but since it is not easy to install because of its thickness, it is not primarily used for Internet.

## Twinaxial cable

- A Twinaxial cable, sometimes referred to as Twinax, is similar to a coaxial cable except for the fact that instead of one copper wire, it has 2 copper wires inside.
- The advantage it provides because of having two conductors is lesser cable loss and lesser interference. Unlike coaxial, it is only suitable for short-distanced and high-speed applications.
- One of the key applications of Twinaxial cables is in server rooms for short distanced connections within the racks. It can be directly attached to a server using connectors, and that’s why it’s sometimes referred to as a DAC (Directly Attached Cable) as well. It is a cheaper alternative to using Fiber Optic cable for speed.
- There are 2 types of Twinaxial cables, `Active twinaxial` cable contains electrical components within connectors to boost the signal. it is reccomended for a link length longer than 5m and less than 10m and `Passive twinaxial cable` is a plain wire with no signal booster. it is recommended for link length between 0.5m and 5m

## Fiber cable

- Fiber Optics Cable is a very thin transparent cable made of glass or plastic.
- It transfers the data at the speed of light, and hence it is the fastest means of transferring data. Fiber cable, because of its nature and design, is not prone to much noise or interference.
- For high-quality services, Fibre Cable is the cable of choice. It consists of 2 components, inner core and cladding. The core acts as a waveguide for the light waves, and the light waves travel through the glass core due to total internal reflection.
- The refraction index of the cladding is lower as compared to that of the core to achieve the phenomenon of total internal reflection. Core and cladding are protected by an outer layer of buffer and a plastic jacket.
- it uses an optical light source
- it is a bounded media type, it is longest bounded media type
- its fast and expensive
- they are mostly used when we need to pass a large amount of information or data at a higher speed without any electromagnetic interface we use fiber cable. its more fragile
- these have 2 types: single-mode, multimode

types of fiber optics:

- `single mode fiber optic cable`
- it has a greatest distance of bounded media around 80 km
- it has a `core diameter of 9 microns`
- it has a cladding diameter of `125 microns`
- `multimode fiber optic cable`
- it has a shorter distance than a single mode
- it has a core diameter of `50 or 60.2 microns`, so its bigger than a SMF
- the smaller the size or concentration of the core the more further the signal can transfer

fiber optics connectors:

- `fusion splicing` is used in the termination of fiber cable by using the connectors- `subscriber connector(SC) or lucent connector(LC)`. the lucent connector is half the size of the subscriber connector
- `straight tip connector`
- `mechanical transfer registered jack(MTRJ)`

## termination standard

- Cable termination needs to be performed at the end of the cable for it to be able to connect to an equipment. Network cables need to be terminated in a standard way in order to function properly.
- There are 2 standards followed for Ethernet cables, `TIA/EIA 568A and TIA/EIA 568B`, and these must be terminated according to these standards. These standards define the color codes for the termination pattern within RJ 45 connectors. The cables must be terminated according to the right color scheme. Else it can cause working errors.
- if both the ends of a cable are terminated with the same standard, it is considered as a `straight cable`, whereas if one end is terminated with 568A and the other end is terminated with 568B standard, it is considered as a `crossover cable`.
- 568A scheme: green strips, green, orange stripes, blue, blue stripes, orange, brown stripes, brown
- 568B scheme: orange strips, orange, green stripes, blue, blue stripes, green, brown stripes, brown

## Connector types

- A cable connector is a small device connected at the end of the cable to terminate it in order for it to become pluggable into an electronic device. It is also used to mate two or more cables. For different requirements and purposes, different types of connectors are used.

## fiber optic connector

- there are primarly 4 types of connectors differ by the way they are connected to the cables
- `subscriber connector` is one of the most common types of Fiber cable connectors used at present time because of its ease to use and install. It is also cost-effective. It uses a push-pull design along with a locking unit to secure the connector on the cable. Due to its inexpensiveness, this type of connector is used in areas where the cables need to be changed frequently or need to be installed in larger quantities.
- `Local connector` is similar to the subscriber connector except for the fact that it uses a latch to secure the connector on the cable. It is smaller in size as compared to other connectors and is preferred where space is an issue.
- `Straight Tip connector` uses a rotating lock to secure the connector on the cable but is less popular than Local and Subscriber Connector because of the latter’s ease of use.
- `MTRJ stands for Mechanical Transferred Registered Jack`. It is recently becoming popular in smaller category connectors. It takes 2 fibers and integrates them into one. It looks similar to the RJ45 connector, and hence it is called MTRJ.

## Polish Types for Fiber Cable

- Before terminating the fiber cable, it is polished to remove any dirt, remove scratches from the glass cable and shape the ferrule (a circular component that holds the fiber cable). It is done to ensure minimal data loss occurs when two cables are connected. When two cables are connected, some of the light rays bounce back due to dirt on the joints (return loss) and the rays that are transferred get weakened in density due to the minor air gap between the joints (insertion loss). This problem is solved by polishing the ferrule in order to minimize both losses. There are mainly two types of polish or contact types in Fiber Cables, APC and UPC
- `Angled Physical contact` type, the glass inside the connector is polished at an angle of 8 degrees. APC type provides lower insertion loss and returns loss when compared to UPC because of its angled shape. Moreover, it doesn’t get worn out as quickly as UPC would get when connected and disconnected multiple times. It must be installed properly, though. Since it angles, there are chances of it being installed incorrectly since it is not a symmetrical design. The connection using the APC technique is most secure and tight.
- `Ultra Physical Contact` type, the ferrule is polished in a dome shape, reducing the return loss. These types of connections are used in high-speed transmission applications. The disadvantage of UPC is that when connected and disconnected multiple times, it is prone to more wear and tear, which impacts the performance over a period of time.

## Twisted pair cable connectors

- `RJ11` connector is primarily used in the telecommunication industry. RJ stands for Registered Jack, indicating that it is a standard used in the telecom and data network industry. It is a 6-pin connector, and different versions of RJs have different numbers of connections. RJ11 is typically 6P2C, meaning 6 pins and 2 connections connector, whereas RJ14 is 6P4C and RJ25 is 6P6C. Other RJ connectors have a similar convention as well, where P indicates the number of pins and C indicates the number of connections/conductors.
- `RJ45` connector is primarily used for Ethernet cables for data transfer. It is an 8P8C connector. The cable within the RJ45 connector is terminated using T568A or T568B standards. For a crossover cable, two ends of the cable can be terminated with different standards, and for a straight cable, both ends are supposed to be terminated with the same standard.

## Transceivers/Media Converters

- A transceiver or media converter, as the name suggests, is a device that is used to convert one form of input to another form of output. In other words, it is a device that connects different incompatible media to make them work with one another. Most commonly, media converters/transceivers are used to optimize Fiber usage. That means these are used to convert signals from a copper wire to light rays used by fiber optic cables.

small form-factor pluggable SFP:

- SFP is a compact transceiver used to convert an electrical signal into an optical signal. It acts as an interface between switches, routers or cables sometimes. There are different types of SFP transceivers available. Some can even convert multimode fiber input to single-mode fiber output. The physical and working specifications for SFP are described under MSA (Multi-Source Agreement) by Small Form Factor Committee.
- SFP supports 100/1000Mbps Ethernet, Fiber Channel and SONET communication standards. It supports speeds of up to 4 Gbps.
- `Enhanced Small Form-factor Pluggable or SFP+` is an enhanced version of SFP, supporting speeds of up to 10Gbps. However, it cannot support speeds less than 1Gbps, and if SFP replaces SFP+, it will operate at a speed of 1Gbps and not lower than that.
- `Quad Small Form-factor Pluggable` is like SFP except for the fact that it can carry 4 channels at a time, and each channel has a capacity of 1Gbps. QSFP supports Ethernet, Fiber, InfiniBand, SONET and SDH communication standards. It supports both single-mode and multimode fiber cables.
- `Enhanced Quad Small Form-factor Pluggable or QSFP+` is an enhanced version of QSFP with 4 channels, and each channel has a capacity of 10 Gbps. It has 4 transmitter lanes and 4 receiver lanes and depending upon which ones are in use, it can operate either at 4 x 10 Gbps or 10 x 4 Gbps. One of the advantages is that all 4 channels can be combined to operate at 40Gbps. In other words, if SFP+ is replaced by QSFP+, it will be more cost-efficient since it will take a lesser number of QSFP+ to operate at a particular speed as compared to the number of SFP+ to operate on that same speed.

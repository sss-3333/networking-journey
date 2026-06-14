# OSI (Open Systems Interconnection) Model 

## Why we need a communication model
- For application independence
- Simplifies network equipment management 
- Decoupled innovation

## 7 Layers of the OSI Model

### Top layer - Application (7)
- where network services are given directly to applications 
- known as end user layer
- eg HTTP, FTP, SMTP

### Presentation Layer (6)
- where data is translated to a readable format, and where encryption is handled
- Sometimes known as the syntax layer, translating data between the application layer and the network
- ensures that data is in usable format
- handles encryption, data formatting 

### Session Layer (5)
- manages sessions between different applications
- establishes (starting), maintaing (keeping sessiona live), and terminating (ending) connections
- eg. session management protocols
### Transport Layer (4)
- where end-t-end communicatoin and data integrity is managed (TCP, UDP)
- provides reliable data transfer services to the upper layers
- eg TCP, UDP

### Network Layer (3)
- where routing and forwarding of data packets are managed
- determines how data is sent to the recipient
- manages packet (little parcels that carry data from one device to another) forwarding including routing through intermediate routers
- eg IP addresses, routers

### Data Link Layer (2)
- where node to node data transfer and error detection is managed
- ensures data is transferred correctly between adjacent network nodes
- eg MAC addresses

### Physical Layer (1)
- the physical connectoin betwen devices eg fibres, hubs are managed. 
- Transmits raw bit streams over a physical medium, dealing with the hardware connection including cables, switches, and netwrok interface cards eg copper, electric signals, fibre lights, waves, wifi (radio frequency).
- No device addressing in this layer (solved bvy data link layer (2))


## TCP/IP Model

Made up of:

- Application Layer (4)
    - where network applications and their protocols operate eg HTTP

- Transport Layer (3)
    - Where end-to-end communication and data transfer between devices happen

- Internet Layer (2)
    - responsible for logical addressing and routing data across different networks eg IP

- Network Access Layer
    - encompasses physical and dating aspects 

## OSI Layers: POV of Sender & Receiver (POST request)

### Example (POV of sender)

Application -> User sends a POST request with JSON data to a HTTP server
Presentation -> serialise JSON to flat byte data strings (conversion)
Session -> Request to establish TCP connection / TLS via HTTPS
Transport-> delivers data cross network via a SYN request to target port 443 (used for HTTPS)
Network -> SYN reqeust is placed in an IP Packet and adds the source / destination IP
Data Link -> wraps packet into frame, adding source/destination MAC addresses to find destination across local networks
Physical -> Data is converted into physical singal eg radio signal, electrical signla, light. 

### Example (POv of receiver)

Physical -> incoming signal is converted into digital bits so computer can understand
Data Link -> bits from layer 1 are assembled into frame
Network -> frame from layer 2 is assembled into IP packets
Transport -> IP packets from layer 3 are assembled into TCP segments 
Session -> connection is established if necessary
Presentation -> decrypt and decompress the data received into suitable fomrat
Application -> data reached intended application. Interprets the HTTP request and processes it accordingly




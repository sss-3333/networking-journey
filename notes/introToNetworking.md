# Introduction To Networking 

## Overview of Computer Networks 

### What is a computer network 
- A group of devices connected to each other, allowing them to share information and resources. 

### Types of Computer Networks
- Local Area Network (LAN) eg home network - small and covers a limited area
- Wide Area Network (WAN) eg home, schools and business network - covers a wide area

### Why are networks important 
- Enable communication between devices
- Let us browse the web, stream movies, and communicate with others
- Allow us to share resources eg printer, shared files
- crucial for internet functionality eg browsing
- Backbone for app connectivity and data transfer

### Importance of netwroks in DevOps
- enables interaction/communication between different servers
- allows you to manage the deployment of applications effectively eg launching and updating 
- crucial in monitoring and managing infrastcutre; spotting issues and fixing them quickly
- essential for optimisation, enhacning performance by ensuring that data flows smoothly between devices and servers, troubleshooting and scalability

## LAN & WAN

### LAN
- connects devices within small areas such as homes for internet access, printer communication. 

### WAN
- covers a larger area like cities, countries, connects multiple LANs

## Switchers, Routers and Firewall 
- These three are what form the backbone of any network

### Switch
- acts as a manager for a LAN, ensuring data flows smoothly eg copmuters, printers.

### Router
- acts as a traffic cop for networks, directing traffic between different networks, eg home network to internet

### Firewall
- acts as a security guard, monitoring and controlling incoming and outgoing network traffic based on predetermined security rules, protecting networks from unauthorised access. 

## IP address & MAC address

### IP (Internet Protocol) address
- Unique identifiers for devices on a network, allowing devices to locate and communicate with each other. 

- IPv4 - most common eg 192.168.0.5, 32-bit number, four decimal numbers ranging from 0-255, provinjg ~4.3 billion unique addresses. Becoming scarce with the rapid growth of the internet. 
- IPv6 - 128-bit address, eight groups of four hexadecimal digits(numbers and letters) spereated by colons rg 2001:0db8:85a3:0000 etc.
    - not only do IPv6's provide more addresses, they also include enhancements like simplified address assignment

### Why IP addresses are important
- enable devices to identify and communicate with each other on the network

### MAC (Media Access Control) Address
- unique identifier assigned to network interfaces
- 48-bit address, seperated by colons eg 00:1A:2B:3C:4D:5E
- Operated at the data link layer, facilitating device ifentification within a local network. Useful for ensuring devices have connected to the correct router, so data packets get to the right place.

## Ports & Protocols

### Ports
- acts as doors. Logical enpoints for communication. When computer is sending data, ports ensure they reach the right place

### Protocols
- rules governing data transmission. define the format of data too. act as languages.

### Importance of ports and protocols 
- facilitate communication between devices. 

### TCP (Transmission Control Protocol)
- A fundamental protocol of internet protocols.  Acts like a postman, ensuring data sent from one device to another reaches accurately and in the correct order. Its a set of rules which devices follow to communicate with each other.
- Some key charactersitics indlude: 
    - connection-oriented - meaning before any data is sent, a connection needs to be established. 
    - requires handshake (three-step) to confirm both devices are ready to sned and receive data.
    - reliable data transfer
- Functionalities:
    - ensures data is delviered in order
    - error-checking and flow control to prevent congestion
    - any bidirectional communication

### UDP (User Datagram Protocol)
- simple protocol to send and receive data
- no prior communication needed, no connection establishment required
- no guarantee that data will reach destination
- fast but less reliable sinco no connection setup
Functionality:
    - Suitable for real-time applications eg video streaming, online gaming
    - Used where speed is more imprtant than reliablity
    - Used for DNS
    - Used for VPN

### TCP vs UDP
- Connection-oriented vs connectionless
- Reliable vs not reliable 
- Slow vs Fast
- Error Checking vs No Error Checking
- Used for web browsing, emailing vs used for video streaming, online gaming, DNS, VPN

Port typically used for HTTP?
80

Port typically used for HTTPS? 
443





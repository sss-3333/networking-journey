# Subnetting 

## What is subnetting / importance
- Dividing one large network into smaller, more manageable subnetworks
- Improves network management and efficiency

## CIDR (Classless Inter-Domain Routing) Notation
- A method for allocating IP addresses and routing IP packets
- Format: Ip_addres/prefix_length. Prefix_length indicates the first 24 bits of the network that are part of the address. Remaining bits go to host adresses.
- Example: 192.168.1.0/24

## Binary: 1s and 0s
- A base-2 number system that uses digits 0 and 1, each digit is known as a bit
- E.g. Converting 101010 to decimal --> start with number on far right ((0) * 2^0) * 0 = 0  --> Then next number from right ((1) * 2^1) * 1 = 2 
--> ((2) * 2^1) * 1 = 2 etc

### Binary and IP addresses

Example: Converting 192.168.1.1 in binary
- 192 / 2 until rached 0, noting remainders
--> 192 / 2 = 90
--> 96 / 2 = 48
--> 48 / 2 = 24
--> 24 / 2 = 12
--> 12 / 2 = 6
--> 6 / 2 = 3
--> 3 / 2 = 1, remainder 1
--> 1 / 2 = 0, remainder 1
--> Therefore binary are remainder numbers 1s and 0s from bottom = 11000000

## Calculating Subnets
Calculating subnets allow u sto identify which part of an IP address is the network portion and which is the host portion

### Subnet Masks
Defines network and host portions 

## NAT (Network Address Translation)
- Translates private IP addresses to public IP addresses
- Facilitates communication between internal network and the internet

### NAT Process
1. Internal device that uses a private IP address (192.168.1.10) wants to send send data to a target source eg website with different IP address (172.217.1.46)
2. Router translates private IP to public IP (192.168.1.10) is translated to (98.117.53.254)
3. The translated IP address becomes the target sources IP address
4. Router translates new IP address back to original IP address as the Target source
5. Source gets original target IP address

### Types of NAT
- Static NAT - maps a single proivate IP address to a single public IP address. (1-to-1 mapping)
- Dynamic NAT - maps a private IP address to one of many pubic IP addresses (1-to-many mapping)
- PAT (Port Address Translation) - allows multiple devices on a local network to be mapped to a single public IP address, but with different port numbers

### Benefits of NAT
- Conserves public IP addresses
- Provides an additional layer of security by hiding internal IP addresses
- Simplifies network design and management by allowing the use of private IP addresses internally while only exposing the necessary public IP addresses.

The three standard streams in networking?
TCP, UDP, ICMP












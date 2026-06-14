# DNS (Domain Name System)

## What is DNS
Translates domain names to IP addresses, similar to phone contacts (names instead of numbers). Essential for accessing websites and services, simplifying navigation on the internet. 

## DNS Componenets

### Component 1: Name Servers
- Load DNS settings and configurations 
- Can be authoritative or recursive
- Authoritative servers - hold the actual DNS records. When queried, provide the definitive answer such as the IP address for a domain name.
- Recursive servers - do NOT hold DNS records theirself. Instead, they query the other name servers on behalf of the client to find the correct DNS record. Can also catch the information they retrieve to speed up future queries. 

### How to find name servers of a certain domain in terminal 

'dig ns (domain name)' e.g. dig ns google.com
For a shorter output -> 'dig +short ns (domain name)'


### Component 2: Zone files
- Stored inside a name service; contain information about the domain 
- help name servers answer queries about how to get to a domain if the name server doesnt know the answer directly
- organise DNS information in a readable format

### Example of a zone file

example.com.          IN   SOA              ns.example.com. 
(Domain name)      (type of record)         (name servers)


### Component 3: Records
- Zone files contain multiple resource records
- Each record contains specific info about hosts, name servers etc
- Other componenets of resource records include:
    - Record name: the domain name being queries
    - TTL (Time To Live): Indicates how long the record is valid before refresh is required
    - Class: Namespace of the record information
    - Type: Type of record (A or MX or AAAA etc)
    - NS - Name server Record
    - Data: The actual info corresponding to the record type. Like IP address for an A record

### Types of records

-A (address record): maps a domain name to an IPv4 address. Most commong eg google.com -> 216.58.204.79
-AAAA: Maps a domain name to an IPv6 address e.g. google.com -> 2a00:1450:4009:81d:200e
-CNAME: Alias of one name to another. It allows you to point multiple domain names to the same IP address eg www.google.com -> google.com
-MX: Specifies the mail server responsible for receiving email for domain e.g. google.com -> mailserver.google.com
-TXT: allows domain admins to insert any text into DNS. Used for vrificatoin purposes and to hold SPF (Sender Policy Framework) data e.g. google.com -> "v=spf1 include.com~all"

## How does DNS work
DNS Resolution -> the process of converting domain names to IP addresses

### DNS Hierarchy and Distribution
A hierarchy that ensures when a a web address is typed into browser, it can quickly find the right IP address

                                  DNS Root (the boss)
                                TLDs (Top Level Domains)
                    Authoritative Name Servers Host 1+Zones for Domains
                                        Domain

DNS Root - contains top level info of where to find the TLDs, no details
TLD - stores info only on domains in that TLD
Authoritative Name Servers Host
Domain - contain zones and zone files

### DNS Resolution Process

1. User types web address into browser 
2. ---> browser sends a request to a DNS resolver that is local to you 
3. ---> DNS resolver does a query. It starts looking for IP address in the local cache 
4. ---> if not found in cache, resolver then queries a root server for the IP address 
5. ---> resolver then queries a .com TLD server
6. ---> TLD server doesn't know the exact IP address of google.com, but knows which authoritative name server to ask
7. ---> Finds a server that has a definitive IP address
8. ---> IP address is returend to DNS resovler
9. ---> DNS resolver sends IP address back to browser
10. ---> Browser can now connect to web address
Tip: A non-authoritative answer means the IP address came back from a cache, otherwise it came directly from the authoritative DNS server


### Importance of DNS Resolution 
- Ensures service availability
- Essential for toubleshooting DNS issues
- Critical for configuring and managing network services

### Domain Registrar
An entity that allowd the purchase and register of domains. Communicates with the TLD registry to manage domain registrations. 

### DNS Hosting Provider
An entity that operates DNS name servers that host DNS zones. Allow for the management of records within zones.

## Network Debugging Tools: 'nslookup' and 'dig'

'nslookup' -> used for querying DNS servers e.g 'nslookup www.google.com'
'dig' (domain information groper) - more detailed and advanced version of nslookup, providing both question and answer sections e.g. 'dig www.google.com'
'dig +short (domain name)' -> provides shorter version of info
'dig +short ns (domain name)' -> provides name servers of that domain

## /etc/hosts File

/etc/hosts is a local file on the computer that maps domain names to IP addresses, allowing us to override DNS settings for specific entries by providing alternative IP addresses.  

### To edit /etc/hosts
Open file with text editor (usually requires admin priveleges) --> add an entry using the format: 'IP_address domain_name' e.g. 127.0.0.1 example.com






# Troubleshooting

## Why troubleshoot
- Ensure smooth operation
- Identify and fix network problems
- Minimise downtime (when services or networks become unavailable)

## Common Network Issues
- Connectivity Loss
- Slow network performance
- IP address conflicts
- DNS Resolution failures

## Example: Connectivity Loss

Symptom: Devices can't access the network
Steps to Diagnose:
    - Check physical connections
    - Verify network configuration
    - Test with ping command

## Troubleshooting with network tools
- ping
- traceroute
- nslookup

### ping command
- Used to test any connectivity between devices
Sunaytx: 'ping [IP address or domain]' e.g. 'ping google.com' --> should give response from domain if internet is working fine

### traceroute command
- Tracks the path data takes to reach a certain destination
- Syntax: 'traceroute  (domain)' or 'tracert (domain)' e.g. 'tracert google.com' --> should give outputs of where its actually going

### nslookup
- Used for querying DNS to find an IP address associated with domain name
- Syntax: 'nslookup (domain)'

### Practical Example and Appraoches to Take in Order
Example: 'I can't reach a website, how can I troubleshoot?'
Step 1: 'ping (domain)' to ensure newtork connectivity is fine
Step 2: 'nslookup (domain)' to ensure no issues with DNS
Step 3: Check host file for overwriting entries
Step 4: Check fireqwall rules; ensure firewall is not blocking any outgoing or incoming traffic
Step 5: Restart browser
Step 6: Chewck DNS Cache, clear if necessary
Step 7: Check system logs; do a tracerout 


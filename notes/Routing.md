# Routing 

## What is Routing / Importance / Process
- The process of determining paths for data to travel across networks
- Ensures data reaches its destination efficiently, improves overall performance optimisation by reducing latency
- Fundamental for internet functionality 
- Ensures reliable application delivery
- Crucial for managing complex infrastructure

### Process of Routing 
- Use routing tables to make decisions

### Example 
Computer sends message / request --> Data first hits router --> Router checks its routing table to find best path --> Starts with routers first network --> Then Network 2, 3, 4 but can hop between routers too --> Until it reaches computer 2

## Static vs Dynamic Routing 

### Static Routing
- Manually configured routes by network admins. Data has a fixed map to follow
- Simple to set up, good for small and stable setups
- Reliable but doesn't adapt well to changes in network

### Dynamic Routing 
- Uses algorithims and complex protocols to automatically find the best path for data, based on current network conditions
- Flexible, scalable and adapts well to network changes. Suitable for larger networks
- Common examples include OSPF (Open Shortest Path First), BGP (Border Gateway Protocol)

## Common Routing Protocols

Routing protocols -> algorithms that automate route determination for data to travel across a network, enhancing network efficiency, by ensuring data takes the most efficient path

### OSPF (Open Shortest Path First)
- Finds the shortest path for data to travel 
- Uses link state information to make routing decisions, considering status, links and costs of a network
- Vast convergence meaning it cna quickly recalculate routes

### BGP (Border Gateway Protocol)
- used to route data between different autonomous systems
- uses a path vector mechanism, meaninng it maintains the path information that gets updates dynamically as the network topology changes
- allows network admins to define routing policies based on various attributes





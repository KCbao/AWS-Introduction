# Elastic Load Balancer
AWS offers 3 types of Load Balancer
* Application Load Balancer: used for load balancing HTTP and HTTPS traffic
* Network Load Balancer: for TCP and high performance
* Classic Load Balancer: for HTTP/HTTPS and TCP

## 7 Layer Model- the OSI Model
It is a conceptual framework which describes the functions of a network. 

* Layer 7: Application layer: what the end user sees, HTTp, web browsers. Load Balancer is operating at this layer
* Layer 6: Presentation layer: data is in a usable format. Encrytion, SSH. 
* Layer 5: Session: maintains connections and sessions
* Layer 4: Transport: transmits data using TCP and UDP.
* Layer 3: Network layer: logically routes packets, based on IP address
* Layer 2: Data LInk: physically transmits data based on MAC addresses
* Layer 1: Physical: Transmits bits and bytes over physical devices. 
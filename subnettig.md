## Subnetting in Networking

* In networking 
    - The process of during a single network into multiple sub networks is called as **Subnetting**

### Subnet ID-

* Each sunet has its unique network address know as its **Subnet ID**
* The subnet ID is created by brrowing some bits from the Host ID part of the IP Address
* The number of bits borrowed depends on the number os subnets created.

### Types of Subnetting 

1. **Fixed Length Subnetting(FLSM)**
      * All the subnets are same size.
      * All the subnets have equal number of hosts.
      * All the subnets have same subnet mask 
Note: 
*
   -   Network ID: frist address of the Network 
   -   Bradcast ID: last address of the Network 
   -   Last usable IP address
   -   Sub net mask : to diff network and host
   -   subnetting can be done based on requriement.
           -   Requierment of Host:     2^n - 2 >= requriement 

1. **Variable Length Subnetting(VLSM)**
      * All the subnets are of same size.
      * All the subnets do not have equal number of hosts.
      * All the subnets do not have same subnet mask

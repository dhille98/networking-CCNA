## Frist Hop Redundancy Protocols 

* A frist hop redundancy protocol(FHRP) is a computer networking protocol which is designed to protect the default default gateway used on a subnetwork by allowing two or more routers to provide backup for that address; in the event of failure of an active router, the backup router will take over the address, usually within a few seconds .

* **Summery:**
* A **virtual IP** is configured on the two routers, and a **virtual MAC** is generated for the virtual IP (each FHRP uses a diffrent format for the virtual MAC)
* An **Active** router ans a **Standby** router are elected.(diffrent FHRPs use diffrent terms)
* End hosts in the network are confiured to use the virtual IP as their default gateway.
* The active router replies to ARP requests using the virtual MAC address, so traffic destined for the other networks will be sent to it.
* if the active router fails, the standby becomes the next active router. 
  
  the new active router will send **gratuitous ARP**  messages so that switches will update their MAC address table. it now functions as the default gatway.

* if the old active router come back online, by default it won't take back its role as the active router. it will become the standby router.


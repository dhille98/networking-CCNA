# Spanning Tree Protocol (STP)

* **Redundacy in Layer 2 Switched networks**
    * Redundancy is an important part of the hierarchical design for eliminating single points of failure and preventing disruption of network service to users.
    * Path redundancy provides multiple network service by eliminating the possibility of a single point of failure
* **Issues with Redundant switch Links**
    * Whenn multiple paths exits between two devices on an Ethernet network, and there is no spanning tree implementation on the switches, alayer 2 `Loop occurs`
    * A Layer 2 loop can result in MAC address table instability, link saturation, and high CPU utilization on switches and end-devices, resulting in the network becoing unusable.

* **Bridging loop solution**
    * we should maintain only one link between switches(no redundancy)
    * use mulriple link between switches and shutdown/disable extra link temporary
        1. manually disable extra link (shutdown command) --> limitation again 
        2. automatically block extra links path using spanning Tree 

### STP 
* using on STP avoide the steps to Loop-free Topolgy
* Spanning Tree Protocol (STP) is a Layer 2 network protocol used to prevent looping within a network topology
* To implement Spanning tree protocol(STP) to builds a loop-free topology there are four steps involved 
      1. Elect the root bridge/switch
      2. Elect the root ports
      3. Elect designated ports
      4. Elect altemate (blocked) ports

* **How STA and STP works ?**
  * During STA and STP functions, switches use `Bridge Protocol Data Units (BPDUS)` TO share information about themselves and their connections. BPDUS are used to elect the root bridge, root ports, designated ports, and alternatte ports
  * Each BPDU contains a bridge ID (BID) that identifies which switch sent the BPUDU to elect root bridge as well as ports
  * default bridge priority for any switch: 32766
  * note that switch haveing lower bridge ID is consider as a root bridge/switch
  * **Extended System ID:** the extended system ID value is a decimal value added to the bridge priority value in the BID identify the VLAN for this BPDU 



* **Key Facts - STP**

* Original STP (802.1D) was created to prevnt loops.
* Switches send probes into the network to discover loops.
* These probes are called as BPDU.
* BPDU = Bridge Protocol Data Unit.
* BPDU will have specific information about the switch.
* Switch multicasts BPDU probes (every 2 seconds) and if it recevives its own BPDU back it means there is a loop in the network 
* Also the BPDU probes helps to elect the root bridge.
* All switches will find the best way to reach the root bridge and the redundant links will be blocked.(Port cost)
* This redundant links will be active only if the exting links or ports goes down 
* 


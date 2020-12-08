# Lab Network Information

## Operational Networks

There are 3 operational networks within the lab. These are the networks used for
general access, management, control, and booting of the test nodes. Note, these
are **not** the networks used for test traffic (i.e. the fabrics between the
test nodes).  All operational networks support both IPv4 and IPv6, and all hosts
generally have golobally resolvable host names.  The domain for the FSDP lab is
**ofa.iol.unh.edu**.

1. VPN Network **10.8.2.0/24**: this is the network all VPN clients reside on.
2. IPMI Network **10.12.1.0/24**: this is the network connected to the IPMI type
interfaces on all bare-metal nodes. Note, the IPMI host name is generally the
systems host name folowed by *"-ipmi"*.
3. Lights Out (lom0) **10.12.2.0/24**: this is the system network, i.e. hosts boot
over and are accessed via this network.

## Fabric Networks

TBD

## Host / Node Information

Each of the bare-metal test nodes in the lab will generally have interfaces on
each of the operational networks and 1 or more of the fabics. More detailed
information about each of the installed NICs is listed on the
[Test Nodes](test_nodes.md) page.

| Host Name | Description | IPMI Network | lom0 Network | IB Fabric | ROCE Fabric | OPA Fabric | iWARP Fabric |
| --------- | ----------- | ------------ | ------------ | --------- | ----------- | ---------- | ------------ |
| beaker| Beaker server and lab controller (VM) | 10.12.1.253 & 2606:4100:3880:3101::253 | 10.12.2.253 & 2606:4100:3880:3102::253 | | | | |
| builder-00 | Build server (bare-metal) | 10.12.1.252 & 2606:4100:3880:3101::252 | 10.12.2.252 & 2606:4100:3880:3102::252 | | | Intel NIC | |
| pdu-1 | Power Distribution Unit #1 | 10.12.1.250 & 2606:4100:3880:3101::250 |
| pdu-2 | Power Distribution Unit #1 | 10.12.1.251 & 2606:4100:3880:3101::251 |
| node-01 | Test Node #01 | 10.12.1.5 & 2606:4100:3880:3101::5 | 10.12.2.5 & 2606:4100:3880:3102::5 | | Intel NICs | Intel NIC | |
| node-02 | Test Node #02 | 10.12.1.10 & 2606:4100:3880:3101::10 | 10.12.2.10 & 2606:4100:3880:3102::10 | | Intel NICs | Intel NIC | |
| node-03 | Test Node #03 | 10.12.1.15 & 2606:4100:3880:3101::15 | 10.12.2.15 & 2606:4100:3880:3102::15 | | Chelsio NIC | Intel NIC | |
| node-04 | Test Node #04 | 10.12.1.20 & 2606:4100:3880:3101::20 | 10.12.2.20 & 2606:4100:3880:3102::20 | | Chelsio NIC | Intel NIC | |
| node-05 | Test Node #05 | 10.12.1.25 & 2606:4100:3880:3101::25 | 10.12.2.25 & 2606:4100:3880:3102::25 | | Chelsio NIC | | |
| node-06 | Test Node #06 | 10.12.1.30 & 2606:4100:3880:3101::30 | 10.12.2.30 & 2606:4100:3880:3102::30 | | Chelsio NIC | | |
| node-07 | Test Node #07 | 10.12.1.35 & 2606:4100:3880:3101::35 | 10.12.2.45 & 2606:4100:3880:3102::35 | | | | |
| node-08 | Test Node #08 | 10.12.1.40 & 2606:4100:3880:3101::40 | 10.12.2.40 & 2606:4100:3880:3102::40 | | | | |
| node-09 | Test Node #09 | 10.12.1.45 & 2606:4100:3880:3101::45 | 10.12.2.45 & 2606:4100:3880:3102::45 | | | | |
| node-10 | Test Node #10 | 10.12.1.50 & 2606:4100:3880:3101::50 | 10.12.2.50 & 2606:4100:3880:3102::50 | | | | |

## Power Control

For the bare-metal test nodes in the lab, power control is primarily through IPMI.
Additional, the bare-metal systems are also each powered through the PDU (power
distribution units), which enable remote control of each "outlet."  Please be
**extremely** careful using the PDU to reboot a host, to avoid "pulling" the power
out from under a node you did not indend.  Each node has only a single power supply!

* [http://pdu-1.ofa.iol.unh.edu User Interface](http://pdu-1.ofa.iol.unh.edu)
* [http://pdu-2.ofa.iol.unh.edu User Interface](http://pdu-2.ofa.iol.unh.edu)

| Host Name | Power Controlled Outlet |
| --------- | ----------------------- |
| builder-00 | PDU-1 Load #23 |
| node-01 | PDU-1 Load #19 |
| node-02 | PDU-2 Load #19 |
| node-03 | PDU-1 Load #18 |
| node-04 | PDU-2 Load #18 |
| node-05 | PDU-1 Load #17 |
| node-06 | PDU-2 Load #17 |
| node-07 | PDU-1 Load #16 |
| node-08 | PDU-2 Load #16 |
| node-09 | PDU-1 Load #15 |
| node-10 | PDU-2 Load #15 |

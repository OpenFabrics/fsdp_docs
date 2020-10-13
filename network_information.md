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
each of the networks.  

| Host Name | Description | IPMI Network | lom0 Network | IB Fabric | ROCE Fabric | OPA Fabric |
| --------- | ----------- | ------------ | ------------ | --------- | ----------- | ---------- |
| beaker| Beaker server and lab controller (VM) | 10.12.1.253 & 2606:4100:3880:3101::253 | 10.12.2.253 & 2606:4100:3880:3102::253 |
| builder-00 | Build server (bare-metal) | 10.12.1.252 & 2606:4100:3880:3101::252 | 10.12.2.252 & 2606:4100:3880:3102::252 |
| pdu-1 | Power Distribution Unit #1 | 10.12.1.250 & 2606:4100:3880:3101::250 |
| pds-2 | Power Distribution Unit #1 | 10.12.1.251 & 2606:4100:3880:3101::251 |

## Power Control

For the bare-metal test nodes in the lab, power control is primarily through IPMI.
Additional, the bare-metal systems are also each powered through the PDU (power
distribution units), which enable remote control of each "outlet."  Please be
**extremely** careful using the PDU to reboot a host, to avoid "pulling" the power
out from under a node you did not indend.  Each node has only a single power supply.

| Host Name | Power Controlled Outlet |
| --------- | ----------------------- |
| builder-00 | PDU-1 Load #23 |

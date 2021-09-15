# Ethernet Fabrics

The following information is for the Ethernet based fabrics (ROCE and iWARP)
hosted in the lab.

## Switch & Fabric

The Ethernet fabric is created with the EdgeCore Wedge 100BF-32X-O-AC, which is
a 32-port, 100G whitebox Ethernet switch.  The switch is currently running
SONiC.master.184-dirty-20210424.033218 version of [SONiC](https://azure.github.io/SONiC/).

The switch's management interface can be accessed via **edgecore.ofa.iol.unh.edu** (10.12.1.248).

In the port definitions below, the power numbers refer to the 40G / 100G port. When
that port is connected to a breakout cable, either to 10G or 25G, the physical
sub-port is indicated as the second number.  *Logical ports in SONiC will be updated when available.*

## Fabric "Manager" & Builder

The [builder-00.ofa.iol.unh.edu](bulders.md) acts as the fabric "manager" through port 1 of the Mellanox MCX653106A-HDAT card, which is connected to switch port 22.

## Test Nodes

The following [test nodes](test_nodes.md) have **Intel E810-CQDA2 100G 2-port** cards installed in PCI Slot 1.

* node-01.ofa.iol.unh.edu - Connected to switch port 1 + 2
* node-02.ofa.iol.unh.edu - Connected to switch port 4 + 5

The following test nodes have **Intel X722-DA2 10G 2-port** cards installed in PCI Slot 2:

* node-01.ofa.iol.unh.edu - Connected to switch port 3.1 and 3.2
* node-02.ofa.iol.unh.edu - Connected to switch port 3.3 and 3.4

The following test nodes have **Chelsio T6225-CR 2x10/25G 2-port** cards installed in PCI Slot 2:

* node-03.ofa.iol.unh.edu - Connected to switch port 6.1 and 6.2
* node-04.ofa.iol.unh.edu - Connected to switch port 6.3 and 6.4

The following test nodes have **Chelsio T62100-CR 2x40/50/100G 2-port** cards installed in PCI Slot 1:

* node-09.ofa.iol.unh.edu - Connected to switch ports 7
* node-06.ofa.iol.unh.edu - Connected to switch ports 12

The following test nodes have **Broadcom 57404 25G 2-port** cards installed in PCI Slot 2:

* node-05.ofa.iol.unh.edu - Connected to switch port 9.1 and 9.2
* node-06.ofa.iol.unh.edu - Connected to switch port 9.3 and 9.4

The following test nodes have **Broadcom 957508-P2100G 100G 2-port** cards installed in PCI Slot 1:

* node-07.ofa.iol.unh.edu - Connected to switch port 16 and 17
* node-08.ofa.iol.unh.edu - Connected to switch port 18 and 19

The following test nodes have **Mellanox QL41212HLCU 25G 2-port** cards installed in PCI Slot 2:

* node-09.ofa.iol.unh.edu - Connected to switch port 20.1 and 20.2
* node-10.ofa.iol.unh.edu - Connected to switch port 20.3 and 20.4

The following test nodes have **Mellanox MCX631105AN-GDAT 50G 1-port** cards installed in PCI Slot 2:

* node-07.ofa.iol.unh.edu - Connected to TBA
* node-08.ofa.iol.unh.edu - Connected to TBA

The following test nodes have **Mellanox MCX631102AN-ADAT 10/25G 2-port** cards installed in PCI slot 3:

* node-09.ofa.iol.unh.edu - Connected to switch port 21.1 and 21.2

The following test nodes have **Mellanox MCX631105AN-GDAT 50G 1-port** cards installed in PCI Slot 2:

* node-07.ofa.iol.unh.edu - Connected to TBA
* node-08.ofa.iol.unh.edu - Connected to TBA

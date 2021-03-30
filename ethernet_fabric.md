# Ethernet Fabrics

The following information is for the Ethernet based fabrics (ROCE and iWARP)
hosted in the lab.

## Switch & Fabric

The Ethernet fabic is created with the EdgeCore Wedge 100BF-32X-O-AC, which is
a 32-port, 100G whitebox Ethernet switch.  The switch is currently running
SONiC.master.125-dirty-20210216.022428 version of [SONiC](https://azure.github.io/SONiC/).

In the port definitions below, the power numbers refer to the 40G / 100G port. When
that port is connected to a breakout cable, either to 10G or 25G, the physical
sub-port is indicated as the second number.  *Logical ports in SONiC will be updated
when available.*

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

* node-05.ofa.iol.unh.edu - Connected to switch ports 7 and 8
* node-06.ofa.iol.unh.edu - Connected to switch ports 12 and 13

The following test nodes have **Broadcom 57404 25G 2-port** cards installed in PCI Slot 2:

* node-05.ofa.iol.unh.edu - Connected to switch port 9.1 and 9.2
* node-06.ofa.iol.unh.edu - Connected to switch port 9.3 and 9.4

The following test nodes have **Broadcom 957508-P2100G 100G 2-port** cards installed:

PCI Slot 3:

* node-05.ofa.iol.unh.edu - Connected to switch port 10 + 11
* node-06.ofa.iol.unh.edu - Connected to switch port 14 + 15

PCI Slot 1:

* node-07.ofa.iol.unh.edu - Connected to switch port 16 + 17
* node-08.ofa.iol.unh.edu - Connected to switch port 18 + 19

The following test nodes have **Mellanox QL41212HLCU 25G 2-port** cards installed in PCI Slot 2:

* node-09.ofa.iol.unh.edu - Connected to switch port 20.1 and 20.2
* node-10.ofa.iol.unh.edu - Connected to switch port 20.3 and 20.4

The following test nodes have **Mellanox MCX631105AN-GDAT 1-port** cards installed in PCI Slot 2:

* node-07.ofa.iol.unh.edu - Connected to TBA
* node-08.ofa.iol.unh.edu - Connected to TBA

The following test nodes have **Mellanox MCX653106A-HDAT 2-port** cards installed in PCI Slot 3:

* node-07.ofa.iol.unh.edu - Connected to TBA
* node-08.ofa.iol.unh.edu - Connected to TBA

The following test nodes have **Mellanox MCX556A-ECAT 2-port** cards installed in PCI slot 1:

* node-09.ofa.iol.unh.edu - Connected to TBA
* node-10.ofa.iol.unh.edu - Connected to TBA

The following test nodes have **Mellanox MCX631102AN-ADAT 2-port** cards installed in PCI slot 3:

* node-09.ofa.iol.unh.edu - Connected to switch port 21.1 and 21.2

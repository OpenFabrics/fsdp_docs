# InfiniBand Fabric

The following information is for the InfiniBand (IB) Fabrics hosted within the lab.

## Switch & Fabric

The IB fabric is created with the Mellanox Quantum QM8700 HDR IB 40 Port Switch.

The switch's management interface can be accessed via **infiniband.ofa.iol.unh.edu** (10.12.1.247).

In the port definitions below, the power numbers refer to the 40G / 100G port. When
that port is connected to a breakout cable, either to 10G or 25G, the physical
sub-port is indicated as the second number.  *Logical ports will be updated
when available.*

## Test Nodes

The following test nodes have **Mellanox MCX653106A-HDAT 200G 2-port** cards installed in PCI Slot 3:

* node-07.ofa.iol.unh.edu - Connected to Mellanox QM8700 IB switch port 1 *and Edgecore Wedge 100BF-32x Ethernet switch port 8*
* node-08.ofa.iol.unh.edu - Connected to Mellanox QM8700 IB switch port 2 *and Edgecore Wedge 100BF-32x Ethernet switch port 13*

The following test nodes have **Mellanox MCX556A-ECAT 100G 2-port** cards installed in PCI slot 1:

* node-09.ofa.iol.unh.edu - Connected to  Mellanox QM8700 IB switch port 3 *and Edgecore Wedge 100BF-32x Ethernet switch port 11*
* node-10.ofa.iol.unh.edu - Connected to  Mellanox QM8700 IB switch port 4 *and Edgecore Wedge 100BF-32x Ethernet switch port 15*

The following test nodes have **Mellanox CX654106A 200G 2-port** cards installed in PCI slots 1 and 3:

* node-10.ofa.iol.unh.edu - *To be connected to switch port 9*

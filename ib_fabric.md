# InfiniBand Fabric

The following information is for the InfiniBand (IB) Fabrics hosted within the lab.

## Switch & Fabric

The IB fabric is created with the Mellanox Quantum QM8700 HDR IB 40 Port Switch.

In the port definitions below, the power numbers refer to the 40G / 100G port. When
that port is connected to a breakout cable, either to 10G or 25G, the physical
sub-port is indicated as the second number.  *Logical ports will be updated
when available.*

## Test Nodes

The following test nodes have **Mellanox MCX653106A-HDAT 200G 2-port** cards installed in PCI Slot 3:

* node-07.ofa.iol.unh.edu - Connected to switch port 1 + 2
* node-08.ofa.iol.unh.edu - *To be connected to switch port 3 + 4*

The following test nodes have **Mellanox MCX556A-ECAT 100G 2-port** cards installed in PCI slot 1:

* node-09.ofa.iol.unh.edu - Connected to switch port 5 + 6
* node-10.ofa.iol.unh.edu - *To be connected to switch port 7 + 8*

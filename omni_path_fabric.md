# Omni-Path (OPA) Fabric

## Switch & Fabric

The Intel Omni-Path 100SWE24QF2 24-port 100G switch is used for this fabric.
The switch can be reached via: **TBD**  

The fabric manager is the builder-00.ofa.iol.unh.edu host.  The Intel Omni-Path
100HFA016LS card is installed in PCI Slot 1 (note PCI Slot 3 is not available
on this serverbecause of an installed RAID card). The NIC is connected to
switch port 5.

## Test Nodes

The following [test nodes](test_nodes.md) have Intel Omni-Path 100HFA016LS 100G
1-port 16X cards installed PCI Slot 3.

* node-01.ofa.iol.unh.edu - Connected to switch port 1
* node-02.ofa.iol.unh.edu - Connected to switch port 2
* node-03.ofa.iol.unh.edu - Connected to switch port 3
* node-04.ofa.iol.unh.edu - Connected to switch port 4

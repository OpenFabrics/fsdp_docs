# InfiniBand Fabric

The following information is for the InfiniBand (IB) Fabrics hosted within the lab.

## Switch & Fabric

The IB fabric is created with the Mellanox Quantum QM8700 HDR IB 40 Port Switch.

The switch's management interface can be accessed via **infiniband.ofa.iol.unh.edu** (10.12.1.247).

In the port definitions below, the power numbers refer to the 40G / 100G port. When
that port is connected to a breakout cable, either to 10G or 25G, the physical
sub-port is indicated as the second number.  *Logical ports will be updated
when available.*

## Builder

The [builder-00.ofa.iol.unh.edu](bulders.md) includes a Mellanox MCX653106A-HDAT card, with port 2 connected to switch port 40.

## Test Nodes

The fabric switch ports are currently connected as follows.

| Switch Port | Connected To                                                       |
|-------------|--------------------------------------------------------------------|
| 1           | node-05 Mellanox 653106A 200G 2-port VPI Port 1                    |
| 2           | node-06 Mellanox 653106A 200G 2-port VPI Port 1                    |
| 3           | node-03 Mellanox 556A ConnectX-5 VPI 100G Port 1                   |
| 4           | node-04 Mellanox 556A ConnectX-5 VPI 100G Port 1                   |
| 5           | node-10 Mellanox 654106A ConnectX-6 200G 2-port VPI Port 1         |
| 6           | node-09 Mellanox 654106A ConnectX-6 200G 2-port VPI Port 1         |
| 40          | builder-00 Mellanox MCX653106A-HDAT Port 2                         |

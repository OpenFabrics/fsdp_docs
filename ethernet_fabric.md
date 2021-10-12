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

| Switch Port | Sub Port | Connected To  
|-------------|----------|---------------
| 1           | N/A      | node-01 Intel E810-CQDA2 100G 2-port RoCE Port 1
| 2           | N/A      | node-01 Intel E810-CQDA2 100G 2-port RoCE Port 2
| 3           | 1        | node-01 Intel X722-DA2 10G 2-port iWARP Port 1
| 3           | 2        | node-01 Intel X722-DA2 10G 2-port iWARP Port 2
| 3           | 3        | node-02 Intel X722-DA2 10G 2-port iWARP Port 1
| 3           | 4        | node-02 Intel X722-DA2 10G 2-port iWARP Port 2
| 4           | N/A      | node-02 Intel E810-CQDA2 100G 2-port RoCE Port 1
| 5           | N/A      | node-02 Intel E810-CQDA2 100G 2-port RoCE Port 2
| 6           | 1        | node-03 Chelsio T6225 T6 25G 2-port iWARP Port 1
| 6           | 2        | node-03 Chelsio T6225 T6 25G 2-port iWARP Port 2
| 6           | 3        | node-04 Chelsio T6225 T6 25G 2-port iWARP Port 1
| 6           | 4        | node-04 Chelsio T6225 T6 25G 2-port iWARP Port 2
| 7           | N/A      | node-07 Mellanox 653106A 200G 2-port VPI Port 2
| 8           | N/A      | node-08 Mellanox 653106A 200G 2-port VPI Port 2
| 9           | 1        | node-05 Broadcom 57414 25G 2-port RoCE Port 1
| 9           | 2        | node-05 Broadcom 57414 25G 2-port RoCE Port 2
| 9           | 3        | node-06 Broadcom 57414 25G 2-port RoCE Port 1
| 9           | 4        | node-06 Broadcom 57414 25G 2-port RoCE Port 2
| 10          | N/A      | node-03 Mellanox 556A ConnectX-5 100G 2-port VPI Port 2
| 11          | N/A      | node-04 Mellanox 556A ConnectX-5 100G 2-port VPI Port 2
| 12          | N/A      | node-05 Chelsio T62100 T6 100G 2-port iWARP Port 1
| 13          | N/A      | node-06 Chelsio T62100 T6 100G 2-port iWARP Port 1
| 14          | N/A      | node-09 Mellanox 654106A ConnectX-6 200G 2-port VPI Port 2
| 15          | N/A      | node-10 Mellanox 654106A ConnectX-6 200G 2-port VPI Port 2
| 16          | N/A      | node-07 Broadcom 57508 200G 1-port RoCE Port 1
| 17          | N/A      | node-07 Broadcom 57508 200G 1-port RoCE Port 2
| 18          | N/A      | node-08 Broadcom 57508 200G 1-port RoCE Port 1
| 19          | N/A      | node-08 Broadcom 57508 200G 1-port RoCE Port 2
| 20          | 1        | node-09 QLogic FastLinQ QL41000 50G 2-port RoCE Port 1
| 20          | 2        | node-09 QLogic FastLinQ QL41000 50G 2-port RoCE Port 2
| 20          | 3        | node-10 QLogic FastLinQ QL41000 50G 2-port RoCE Port 1
| 20          | 4        | node-10 QLogic FastLinQ QL41000 50G 2-port RoCE Port 2
| 32          | N/A      | builder-00 MCX653106A-HDAT Port 1

Note, node-07 and node-08, PCI2 Mellanox 631105AN 50G 1-port RoCE, are currently missing cables and are not connected.

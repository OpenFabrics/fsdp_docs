# Test Nodes

The following describes the status of each test node in the FSDP cluster,
along with the installed fabric cards, etc.

Users can login to the HPE iLO5 or IPMI interface of each node using their
assigned username / password.  Login to the installed OS on the node is via
the root password they provisioned within beaker prior to the install.  See
the [Network Information](network_information.md) page for IPMI and IP
address details for each node.

[Omni-Path Fabric](omni_path_fabric.md)

[InfiniBand Fabric 0](ib_fabric.md)

[RoCE & iWARP Ethernet Fabric](ethernet_fabric.md)

## Matrix Table of all nodes

| Node Name | PCI Slot | Card                                          | Port | opa0 | ib0 | roce | iw |
|-----------|----------|-----------------------------------------------|------|------|-----|------|----|
| node-01   | 1        | Intel E810-CQDA2 100G 2-port RoCE             | 1    |      |     | x    |    |
|           |          |                                               | 2    |      |     |      |    |
|           | 2        | Intel X722-DA2 10G 2-port iWARP               | 1    |      |     |      | x  |
|           |          |                                               | 2    |      |     |      |    |
|           | 3        | Omni-Path 100HFA016LS 100G 1-port OPA         | 1    | x    |     |      |    |
| node-02   | 1        | Intel E810-CQDA2 100G 2-port RoCE             | 1    |      |     | x    |    |
|           |          |                                               | 2    |      |     |      |    |
|           | 2        | Intel X722-DA2 10G 2-port iWARP               | 1    |      |     |      | x  |
|           |          |                                               | 2    |      |     |      |    |
|           | 3        | Omni-Path 100HFA016LS 100G 1-port OPA         | 1    | x    |     |      |    |
| node-03   | 1        | Mellanox 556A ConnectX-5 100G 2-port VPI      | 1    |      | x   |      |    |
|           |          |                                               | 2    |      |     | x    |    |
|           | 2        | Chelsio T6225 T6 25G 2-port iWARP             | 1    |      |     |      | x  |
|           |          |                                               | 2    |      |     |      |    |
|           | 3        | Omni-Path 100HFA016LS 100G 1-port OPA         | 1    | x    |     |      |    |
| node-04   | 1        | Mellanox 556A ConnectX-5 100G 2-port VPI      | 1    |      | x   |      |    |
|           |          |                                               | 2    |      |     | x    |    |
|           | 2        | Chelsio T6225 T6 25G 2-port iWARP             | 1    |      |     |      | x  |
|           |          |                                               | 2    |      |     |      |    |
|           | 3        | Omni-Path 100HFA016LS 100G 1-port OPA         | 1    | x    |     |      |    |
| node-05   | 1        | Chelsio T62100 T6 100G 2-port iWARP           | 1    |      |     |      | x  |
|           |          |                                               | 2    |      |     |      |    |
|           | 2        | Broadcom 57414 25G 2-port RoCE                | 1    |      |     | x    |    |
|           |          |                                               | 2    |      |     |      |    |
|           | 3        | Empty                                         |      |      |     |      |    |
|           |          |                                               |      |      |     |      |    |
| node-06   | 1        | Chelsio T62100 T6 100G 2-port iWARP           | 1    |      |     |      | x  |
|           |          |                                               | 2    |      |     |      |    |
|           | 2        | Broadcom 57414 25G 2-port RoCE                | 1    |      |     | x    |    |
|           |          |                                               | 2    |      |     |      |    |
|           | 3        | Empty                                         |      |      |     |      |    |
|           |          |                                               |      |      |     |      |    |
| node-07   | 1        | Broadcom 57508 200G 1-port RoCE               | 1    |      |     | x    |    |
|           |          |                                               | 2    |      |     |      |    |
|           | 2        | Mellanox 631105AN 50G 1-port RoCE             | 1    |      |     | x    |    |
|           | 3        | Mellanox 653106A 200G 2-port VPI              | 1    |      | x   |      |    |
|           |          |                                               | 2    |      |     | x    |    |
| node-08   | 1        | Broadcom 57508 200G 1-port RoCE               | 1    |      |     | x    |    |
|           |          |                                               | 2    |      |     |      |    |
|           | 2        | Mellanox 631105AN 50G 1-port RoCE             | 1    |      |     | x    |    |
|           | 3        | Mellanox 653106A 200G 2-port VPI              | 1    |      | x   |      |    |
|           |          |                                               | 2    |      |     | x    |    |
| node-09   | 1&3      | Mellanox 654106A ConnectX-6 200G 2-port VPI   | 1    |      | x   |      |    |
|           |          |                                               | 2    |      |     | x    |    |
|           | 2        | QLogic FastLinQ QL41212 25G 2-port RoCE       | 1    |      |     | x    |    |
|           |          |                                               | 2    |      |     |      |    |
| node-10   | 1&3      | Mellanox 654106A ConnectX-6 200G 2-port VPI   | 1    |      | x   |      |    |
|           |          |                                               | 2    |      |     | x    |    |
|           | 2        | QLogic FastLinQ QL41212 25G 2-port RoCE       | 1    |      |     | x    |    |
|           |          |                                               | 2    |      |     |      |    |

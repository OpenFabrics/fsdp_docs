# Build Servers

The following describes the build server(s) in the FSDP cluster and provides instructions on how to use them.

## Server Information

NOTE: This information can also be found in [network_information.md](network_information.md).

### builder-00.ofa.iol.unh.edu

| Parameter | Value |
|-----------|-------|
| Hostname   | builder-00.ofa.iol.unh.edu|
| System | HPE DL325 |
| lom0 Network | 10.12.2.252 & 2606:4100:3880:3102::252 |
| IPMI Network | builder-00.ipmi.ofa.iol.unh.edu & 10.12.1.252 & 2606:4100:3880:3101::252 |
| ROCE Fabric | Mellanox MCX653106A-HDAT Port 1 *(Connected to Edgecore Wedge 100BF-32x Ethernet switch port 22)* |
| iWARP Fabric | Mellanox MCX653106A-HDAT Port 1 *(Connected to Edgecore Wedge 100BF-32x Ethernet switch port 22)* |
| IB Fabric | Mellanox MCX653106A-HDAT Port 2 *(Connected to Mellanox QM8700 IB switch port 40)*|
| OPA Fabric | Intel Omni-Path 100HFA016LS (fabric manager) |

## Usage Instructions

### Accessing the Server

#### 1. Connect to the VPN

When your FSDP Cluster account is created, you should receive an email
with your OpenVPN client configuration attached.

**Linux Users:** Linux users should use the OpenVPN client supplied with their distribution. Users of modern Linux distributions may import this file as-is into NetworkManager.
When using OpenVPN from the command line, DNS may fail to resolve. There are instructions at the bottom
of the configuration file to try to solve this issue.

**Windows Users:** Install the OpenVPN client from [here](https://openvpn.net/index.php/open-source/downloads.html).
You may use the configuration as-is with this client. You may need to run OpenVPN as administrator for the routes
to be set up correctly once connected.

**Mac Users:** Install TunnelBlick from [here](https://tunnelblick.net). You may need to run with administrative
privileges for the routes to be set up correctly once connected.

**Usage of this VPN connection is contingent upon agreement with the
[UNH-IOL Usage Agreement](https://www.iol.unh.edu/sites/default/files/charters/unh-iol-usage-agreement.pdf).**

**You are expected to be physically present at your local system whenever
it is connected to the VPN.**

**Note that this file contains private key material and you are expected
to keep it appropriately secure. E-mail ofalab@iol.unh.edu
immediately if your VPN credentials have been compromised.**

#### 2. Connect to the build server

Connect to the build server via ssh:

`ssh <username>@builder-00.ofa.iol.unh.edu`

The first time you log in, you should use the initial password given in the welcome email you received.
You will immediately be required to change your password upon first login.

### Running build containers

The containers for Fedora-based images are maintained by the [cki-project](https://gitlab.com/cki-project/containers).
Instructions for accessing and running these images using rootless `podman` can be found below.

#### builder-fedora (Fedora 33)

Run the following command:

`podman run -it registry.gitlab.com/cki-project/containers/builder-fedora`

You should now be running the container image from the registry.

#### builder-rawhide (Fedora 34)

Run the following command:

`podman run -it registry.gitlab.com/cki-project/containers/builder-rawhide`

You should now be running the container image from the registry.

#### builder-rhel7

TBA

#### builder-rhel8

TBA

#### builder-rhel9

TBA

### HTML File Access

To enable cluster users to easily move artifacts from their build environments to
the test nodes, the build servers have been configured to support user public_html
directorys.  You will need to take the following steps to create a public_html
root in your home directory.  Note, any files placed this directory will be made
availble to all logged in users in the cluster, unless you take the steps below
to add a password (http basic authentication).  The steps to enable the password
are optional and at your discretion.

1. Create the directory, `mkdir ~/public_html`
1. Create the .htaccess file with the contents below, `vim ~/public_html/.htaccess`
Note, you need to replace username with your actually username on the system.
1. Create your password, `htpasswd -c ~/public_html/.htpasswd USERNAME`

#### .htaccess file contents

```bash
AuthType Basic
AuthName "Password Required"
Require valid-user
AuthUserFile /home/USERNAME/public_html/.htpasswd
```

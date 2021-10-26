# fsdp_docs

Documentation for the OpenFabrics Fabric Software Development Platform (FSDP)

## Lab Usage

The lab is available to members of the Open Fabrics Alliance, to support the
development and mainteance of fabric drivers and software, as well as the
upstream activities, such as the Linux Kernel.

Usage of the lab is doverned by an [Acceptable Usage Policy](AUP.md)

## Lab Access

External users will connect to the lab and the systems hosted therein over an
openVPN connection.  Once connected, the networks shown below are available to
the user directly over the VPN.  

Unless ohterwise noted, users should have access to each system (test nodes, PDUs,
etc.) in the lab via either their SSH key, or their password.  We are, to the
extend possible, avoiding the use of any shared or published credentials for the
systems.

Users can login to the HPE iLO5 or IPMI interface of each node using their
assigned username / password.  Login to the installed OS on the node is via
the root password they provisioned within beaker prior to the install.  See
the [Network Information](network_information.md) page for IPMI and IP
address details for each node

### A Note About Certificates

The services within the OFA lab / cluster utilize SSL/TLS where possible, with
certificates signed via a common CA provided by IPA. If you wish to utilize local
clients to connect to these services, such as the Beaker Client, you will need to
install and trust the CA certificate locally on your system. You can download the
[ca.crt](https://beaker.ofa.iol.unh.edu/ca.crt) file from the beaker server.

## Lab Logical Network Layout

The figure below shows the general layout of the lab network.  The [Lab Network
Information](network_information.md) page provides additional information about
the lab systems, including lists of host names, etc.

![FSDP Logical Diagram](<figures/FSDP Logical Diagram.png>)

## Getting Started

Each lab user must have an account to access the lab through the OpenVPN
connection.  Accounts should be requested by completing the [Account Creation
Request Form](FSDP_Account_Request.pdf) and submitting the completed form, along
with the user's public SSH key to [FSDP Account Request Email](mailto:fsdp-accounts@openfabrics.org).

Once the account has been created by the lab staff, the lab will notify the user,
by email, providing the temporary, one-time-use password.  As part of the email
notification, the lab will provide an OpenVPN configuration file.

Once connected to the OpenVPN, users can reach the lab resources, including the
[Beaker Server](http://beaker.ofa.iol.unh.edu), lab infrastructure, and the test
nodes.  The [Network Information](network_information.md) page provides
additional details for the resources and hardware within the lab. The
[Test Nodes](test_nodes.md) page describes the systems within the cluser, and the
cards installed and connected fabrics.

Users connecting to the lab for the first time should immedately SSH into the
builder-00.ofa.iol.unh.edu server and follow the prompts to change their
password.  This username and password will be used to access all resources
within the lab.  More information about the build server(s) in the lab is available
on the [Builders](builders.md) page.  The build server(s) may be used by lab
participants to store build environmets, code, and other items that might
be required for their testing, along with providing CPU resources to compile
artifacts for testing.  It provides can provide http access to those artifacts
for easy access by the [Test Nodes](test_nodes.md).

It is recommended each company appoint a primary delegate, who will notify
the OFA and FSDP lab of any staffing changes that require the deactivation or
removal of any FSDP lab accounts.  The [Account Deletion Request
Form](FSDP_Account_Deletion.pdf) should be used for this purpose.

## Copyright

Initial copyright on the repository is (c)2020 Red Hat, Inc.

## Copyright License Grant

The documentation in this repository is licensed as CC BY 4.0.  This
shall apply to all files by default.  It may be overridden on a file by
file basis by specifically stating an alternate license directly in the
file in question.

## Grant of Copyright License by Contributors

All submissions to this repository must use
the [Developer Certificate of Origin](https://developercertificate.org/)
method of Copyright License Grant (so all submissions must include a
Signed-off-by: tag in the commit message).

Compliance with all terms of the DCO are required, including agreement to
license the contribution under the same terms as the existing license on
the files being modified.

Contributors maintain their own copyright ownership and grant the
OpenFabrics Alliance a perpetual license to use their contributions
pursuant to the terms of the DCO.

# vcn4container
terraform script to create vcn for OKE container

In order to create a container on OKE as per documentation, you need to create a VCN with this mimimum configuration 
(the 'Create Virtual Cloud Network plus related resources'  feature in the console is not enough)

- 1 internet gateway
- 1 route table
- 2 public subnet for **loadbalancer**
- 3 public subnet for **worker**
- 1 security rule for **worker** that allows both TCP and UDP traffic between nodes
- 1 security rule for **loadbalancer** that allows access from internet


for details see this document https://docs.us-phoenix-1.oraclecloud.com/Content/ContEng/Concepts/contengnetworkconfig.htm

This terraform script creates all required resources


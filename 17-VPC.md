1- What is a VPC?

- Amazon Virtual Privte Cloud (Amazon VPC) lets you provision a logically isolated section of the Amazon Web Services (AWS) Cloud where you can lanuch AWS resources in a virtual network that you define. You have complete control over your virtual networking environment, including selectrion of your own IP address range, creation of subnets, and configuration of route tables and network getaways.

- You can easily customize the network configuration for your Amazon Virtual Private Cloud. Aditionally, you can create a Hardware Private Network (VPN) connection between your corporate datacenter and your VPC and leverage the AWS cloud as an extension of your corporate datacenter.

2- What can we do with a VPC?

- Launch instances into a subnet of your choosing
- Assign custom ip address ranges ranges in each subnet
- Configure route tables between subnets
- Create internet getaway and attach it to our VPC
- Much better security control over your AWS resources
- Instance security groups
- Subnet network access control lits (ACLS)

4- Default VPC vs. Custom VPC

- Default VPC is user friendly, allowing you to inmediately deploy instances.
- All Subnets instance has both a public and private IP address.
- Each EC2 instance has both a public and private ip address.

5- VPC  PEering

- Allows you to connect one VPC with another via a direct network route using private IP addresses.
- Instances behave as if they were on the same private network
- You can peer VPC's with other AWS accounts as well with other VPC's in the same account
- Peering is in a star configuration: ie 1 central VPC peers with 4 others. (No transitive peering)

- Notes
    - Think of a VPC as a logical datacenter in AWS.
    - Consists of IGWs (Or Virtual Private Getaways), Route Tables,m NEtwork Access Control Lists, Subnets, and Security Groups.
    - 1 Subnet = 1 Availability Zone.
    - Security Groups are Stateful, Network Access Control Lists are Stateless.
    - No Transitive peering

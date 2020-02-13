1- What is a NAT Gateway?

- A NAT instance is a sigle EC2 Instance, a NAT gateway is a highly available gateway that allows you to have your private subnets to comunicate to the internet without going public.

2- Nat instance

- When crating a NAT insance, disable Source/Destination Checks on the instance.
- NAT instances must be in a public subnet.
- There must be a route out of the private subnet to the NAT instance, in order for this to work.
- The amount of traffict that NAT instances can support depends on the instance size. If you are bottlenecing, increase the instance size.
- You can create high availability using Autoscaling Groups, multiple subnets in different AZs, and a script to automate failover.
- Behind a Security Group

3- Nat Gateways

- Redundant inside the Availability Zone
- Preffered by the enterprise
- Starts at 6GBbps and scales currently to 45Gbps
- No need to patch
- Not assocuated with security groups
- Automatically assigned a public ip address
- Remember to update your route tables
- No need to disable Source/Destination Checks
- IF you ahve resoucers in multipel Availability Zones and they share one NAT gateway, in the event that the NAT gateway's Availability Zone is down, resources in the other Availability Zones lose internet access. To create an Availability Zone- independandt architecture, create a NAT gateway in each Availability Zone and configure your routing to ensure that resources use the NAT gateway in the same Availability Zone.

4- Network Access Control List

- Your VPC automatically comes with a default network ACL, and by default it allwos all outbound and inbound traffict.
- You can create custom network ACL's By default, each custom network ACL denies all inbound and outbound traffict until you add rules
- Each subnet in your VPC must be associated with a networ ACL. If you don't explicity associate a subnet with a network ACL, the subnet is automatically associated with the default network ACL.
- Block IP Addresses using network ACLs not Security Groups.
- You can associate a network ACL with multiple subnets, however, a subnet can be associated with only one network ACL at the time. When you associate a network ACL with a subnet. the previous association is removed.
- Network ACLs contain a number list of rules that is evaluated in order, starting with the lowest numbered rule.
- Network ACLs have separate inbound and outbound rules, and each rule can either allow or deny traffic.
- NEtwork ACLs are stateless, responses to allowed inbound traffict are subject to the rules for outbound traffict (and vice versa).

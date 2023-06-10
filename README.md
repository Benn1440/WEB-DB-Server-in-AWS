# AWS VPC NETWORKING CONCEPT

- Explore the components that comprise a Virtual private cloud(VPC)
- Configure a route table attached to a subnet within a VPC
- Configure a route table to direct internet-bound traffic to thee internet gateway
- Configure inbound Rules within a security group to control access

Using Amazon VPC we can easily launch AWS resources into a virtual network that we define.
This Virtual network closely resembles a traditional netrowrk that we operate in a data center (Onpremises) but with the additional scalabitlity infrastructure which AWS provides.

The Web Server, using security group WebServerSecurityGroup, needs to connect to the DB Server, using security group DbServerSecurityGroup, over a TCP connection on port 3306.

Our servers will determine if the Web Server can connect to the DB Server, on port 3306, with Custom Source subnet 10.10.0.0/24.

![DBANDWEB](https://github.com/Benn1440/WEB-DB-Server-in-AWS/assets/67696393/036f41d3-a89d-4f9c-bf86-c1c41beba399)

Configure a subnet, each subnet must reside entirely within one availability zone and cannot span zones

Configure a route Table that contains rules called routes that usually defines where network traffic from the subnet or gateway is directed.
Usually important to use a public subnet for internet connected resources and a private subnet for resources not connected to the internet

![sUBNET](https://github.com/Benn1440/WEB-DB-Server-in-AWS/assets/67696393/d9b88a52-9e7d-4396-a71b-edf8c6eccc38)

Configured a Network address translation NAT gateway which allows instances in a private subnet to connect with services outside the VPC

![DB Rules](https://github.com/Benn1440/WEB-DB-Server-in-AWS/assets/67696393/b64eb325-e806-4af3-bc7a-6dc6360d1e2a)

# Application Running on http://44.214.254.30/

Updated the security group rules, and then review the Java application for a visual confirmation of an established connection. The status should change to Connected. 

![Application Connection](https://github.com/Benn1440/WEB-DB-Server-in-AWS/assets/67696393/9015d337-98ae-4c4e-b5ec-2c7186a39600)

# N.B: Resources on AWS would be deactivated to avoid incurring cost.











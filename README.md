# Active-Directory-Home-Lab

used PowerShell to create users from a given list

Downloaded Oracle VirtualBox to run a virtual machine (VM).

Downloaded the Windows 10 ISO.

Downloaded the Server 2019 ISO.

These will be used to install two different operating systems on two different machines.

VM 1: Domain Controller; It's going to house Active Directory.

VM 2: Network Adapters; one is going to be used to connect to the outside internet, while the other will be used to connect to the VirtualBox (a private network that the clients will be connecting to).

We will be installing Server 2019 on VM1, then assigning IP addressing for the internal network. The external network will automatically get IP addresses from the home network/home routers.

After setting up the IP addressing, the server was named and Active Directory was installed, creating the domain. Then, I configured NAT and Routing so that the clients on the private network can reach the internet through the DC.

Then I set up DHCP on the DC so that when we create our Windows 10 machine, it can automatically receive an IP address.

The last thing I did on the DC before creating a client virtual machine is run a PowerShell script that will automatically create a thousand users in Active Directory.

Created VM2: Installed Windows 10 on it.

It is connected to the private VirtualBox network.

Named that machine Client 1, joined it to the domain, and allowed users to log into it with one of the Domain Accounts.

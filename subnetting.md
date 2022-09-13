
A subnet mask is selected by the network administrator to divide a network into smaller sub-networks. There is no rule how to "calculate" it from an IP address.

Let's look at an example with a very common subnet mask ```255.255.255.0``` which in binary is ```1111 1111.1111 1111.1111 1111.0000 0000```.

A subnet mask will always have a certain number of zeros at the end. Above netmask has 8 zeros at the end, indicating that there will be ```2^8 = 256``` possible addresses in the subnetwork. Sysadmin might want to have a smaller sub-network, so (s)he can choose a subnet mask 
```255.255.255.127``` which is ```1111 1111.1111 1111.1111 1111.1111 0000 ``` and will allow ```2^4 = 32``` addresses in the sub-net.

Edit: A sysadmin will assign a subnet mask to each IP address based on the administrative requirements. This is done during the design of the network. Let's say that sysadmin knows that in the new branch there are 100 people in sales, and 20 in accounting. Also sysadmin knows that he has 10.10.10.0-255 reserved for that branch addresses. So one way a sysadmin can divide 0-255 range is:

10.10.10.0-127   : Sales
10.10.10.128-158 : Accounting
Then the IP addresses and subnet masks will be:

IP: 10.10.10.0-127   MASK: 255.255.255.128    : Sales
IP: 10.10.10.128-159 MASK: 255.255.255.224    : Beancounters
In each address range 2 addresses will not be used for users: 1st one because it is a network number and the last, because it is a broadcast address.

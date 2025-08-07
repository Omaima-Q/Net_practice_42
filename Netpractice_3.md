# Subnet mask

The second item, which is required for TCP/IP to work, is the **subnet mask**.
The **subnet mask** is used by the TCP/IP protocol to determine whether a host is on the local subnet or on a remote network.

In **TCP/IP**, the parts of the IP address that are used as the network and host addresses aren't fixed.
Unless you have more information, the network and host addresses above can't be determined.
This information is supplied in another 32-bit number called a subnet mask.
The subnet mask is 255.255.255.0 in this example.
It isn't obvious what this number means unless you know 255 in binary notation equals 11111111.
So, the subnet mask is 11111111.11111111.11111111.00000000.

Lining up the IP address and the subnet mask together, the network, and host portions of the address can be separated:
```
11000000.10101000.01111011.10000100 - IP address (192.168.123.132)
11111111.11111111.11111111.00000000 - Subnet mask (255.255.255.0)
```
The first 24 bits (the number of ones in the subnet mask) are identified as the network address.
The last 8 bits (the number of remaining zeros in the subnet mask) are identified as the host address.
It gives you the following addresses:
```
11000000.10101000.01111011.00000000 - Network address (192.168.123.0)
00000000.00000000.00000000.10000100 - Host address (000.000.000.132)
```
So now you know, for this example using a 255.255.255.0 subnet mask, that the network ID is 192.168.123.0, and the host address is 0.0.0.132.
When a packet arrives on the 192.168.123.0 subnet (from the local subnet or a remote network), and it has a destination address of 192.168.123.132, your computer will receive it from the network and process it.

Almost all decimal subnet masks convert to binary numbers that are all ones on the left and all zeros on the right. Some other common subnet masks are:

| Decimal           | Binary                                   | CIDR | Host Bits | Usable Hosts|
|-------------------|------------------------------------------|------|-----------|-------------|
| 255.255.255.192   | 11111111.11111111.11111111.11000000      | /26  | 6         | 62          |
| 255.255.255.224   | 11111111.11111111.11111111.11100000      | /27  | 5         | 30          |

| Decimal    | Subnet Mask   | Network Address | Host Range        |
|---------------|---------------|-----------------|-------------------|
| 192.168.1.10  | 255.255.255.0 | 192.168.1.0     | 192.168.1.1-254   |
| 10.0.0.5      | 255.0.0.0     | 10.0.0.0        | 10.0.0.1-254      |
| 172.16.5.20   | 255.255.0.0   | 172.16.0.0      | 172.16.0.1-65534  |

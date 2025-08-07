
# Understand TCP/IP addressing and subnetting basics

## Summary

When you configure the TCP/IP protocol on a Windows computer, the TCP/IP configuration settings require:
```
1. An IP address
2. A subnet mask
3. A default gateway
```
To configure TCP/IP correctly, it's necessary to understand how TCP/IP networks are addressed and divided into networks and subnetworks.

The success of TCP/IP as the network protocol of the Internet is largely because of its ability to connect together networks of different sizes and systems of different types. 

These networks are arbitrarily defined into three main classes (along with a few others) that have predefined sizes. Each of them can be divided into smaller subnetworks by system administrators.

A subnet mask is used to divide an IP address into two parts. One part identifies the host (computer), the other part identifies the network to which it belongs. To better understand how IP addresses and subnet masks work, look at an IP address and see how it's organized.

## IP addresses: Networks and hosts

An IP address is a **32-bit number**. It uniquely identifies a host (computer or other device, such as a printer or router) on a TCP/IP network.

IP addresses are normally expressed in dotted-decimal format, with four numbers separated by periods, such as **192.168.123.132**. To understand how subnet masks are used to distinguish between hosts, networks, and subnetworks, examine an IP address in binary notation.

**For example**, the dotted-decimal IP address **192.168.123.132** is (in binary notation) the 32-bit number **11000000101010000111101110000100**. This number may be hard to make sense of, so divide it into four parts of eight binary digits.

These 8-bit sections are known as octets. The example IP address, then, becomes **11000000.10101000.01111011.10000100**. This number only makes a little more sense, so for most uses, convert the binary address into dotted-decimal format (192.168.123.132). The decimal numbers separated by periods are the octets converted from binary to decimal notation.

For a **TCP/IP** **wide area network (WAN)** to work efficiently as a collection of networks, the routers that pass packets of data between networks don't know the exact location of a host for which a packet of information is destined. Routers only know what network the host is a member of and use information stored in their route table to determine how to get the packet to the destination host's network. After the packet is delivered to the destination's network, the packet is delivered to the appropriate host.

For this process to work, an IP address has two parts. The first part of an IP address is used as a network address, the last part as a host address. If you take the example 192.168.123.132 and divide it into these two parts, you get 192.168.123. Network .132 Host or 192.168.123.0 - network address. 0.0.0.132 - host address.

![ip_addressing](https://github.com/user-attachments/assets/b7a6c5ad-f6c8-4bae-b447-a5832cb7a170)
<svg width="800" height="600" xmlns="http://www.w3.org/2000/svg">


<div style="font-family: ;">Understand TCP/IP addressing and subnetting basics</div>

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


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
  <!-- Background -->
  <rect width="800" height="600" fill="#f8f9fa" stroke="#dee2e6" stroke-width="2"/>
  
  <!-- Title -->
  <text x="400" y="30" text-anchor="middle" font-family="Arial, sans-serif" font-size="24" font-weight="bold" fill="#212529">IP Addresses: Networks and Hosts</text>
  
  <!-- IP Address Example -->
  <text x="50" y="70" font-family="Arial, sans-serif" font-size="16" font-weight="bold" fill="#495057">Example IP Address: 192.168.123.132</text>
  
  <!-- 32-bit representation -->
  <text x="50" y="100" font-family="Arial, sans-serif" font-size="14" fill="#6c757d">32-bit binary representation:</text>
  <rect x="50" y="110" width="700" height="40" fill="#e9ecef" stroke="#adb5bd" stroke-width="1" rx="5"/>
  <text x="400" y="135" text-anchor="middle" font-family="Courier New, monospace" font-size="16" font-weight="bold" fill="#dc3545">11000000101010000111101110000100</text>
  
  <!-- Octets breakdown -->
  <text x="50" y="180" font-family="Arial, sans-serif" font-size="14" fill="#6c757d">Divided into 4 octets (8 bits each):</text>
  
  <!-- Octet 1 -->
  <rect x="50" y="200" width="150" height="60" fill="#d1ecf1" stroke="#bee5eb" stroke-width="2" rx="5"/>
  <text x="125" y="220" text-anchor="middle" font-family="Courier New, monospace" font-size="14" font-weight="bold" fill="#0c5460">11000000</text>
  <text x="125" y="240" text-anchor="middle" font-family="Arial, sans-serif" font-size="18" font-weight="bold" fill="#155724">192</text>
  <text x="125" y="255" text-anchor="middle" font-family="Arial, sans-serif" font-size="12" fill="#6c757d">Octet 1</text>
  
  <!-- Octet 2 -->
  <rect x="220" y="200" width="150" height="60" fill="#d1ecf1" stroke="#bee5eb" stroke-width="2" rx="5"/>
  <text x="295" y="220" text-anchor="middle" font-family="Courier New, monospace" font-size="14" font-weight="bold" fill="#0c5460">10101000</text>
  <text x="295" y="240" text-anchor="middle" font-family="Arial, sans-serif" font-size="18" font-weight="bold" fill="#155724">168</text>
  <text x="295" y="255" text-anchor="middle" font-family="Arial, sans-serif" font-size="12" fill="#6c757d">Octet 2</text>
  
  <!-- Octet 3 -->
  <rect x="390" y="200" width="150" height="60" fill="#d1ecf1" stroke="#bee5eb" stroke-width="2" rx="5"/>
  <text x="465" y="220" text-anchor="middle" font-family="Courier New, monospace" font-size="14" font-weight="bold" fill="#0c5460">01111011</text>
  <text x="465" y="240" text-anchor="middle" font-family="Arial, sans-serif" font-size="18" font-weight="bold" fill="#155724">123</text>
  <text x="465" y="255" text-anchor="middle" font-family="Arial, sans-serif" font-size="12" fill="#6c757d">Octet 3</text>
  
  <!-- Octet 4 -->
  <rect x="560" y="200" width="150" height="60" fill="#d4edda" stroke="#c3e6cb" stroke-width="2" rx="5"/>
  <text x="635" y="220" text-anchor="middle" font-family="Courier New, monospace" font-size="14" font-weight="bold" fill="#0c5460">10000100</text>
  <text x="635" y="240" text-anchor="middle" font-family="Arial, sans-serif" font-size="18" font-weight="bold" fill="#721c24">132</text>
  <text x="635" y="255" text-anchor="middle" font-family="Arial, sans-serif" font-size="12" fill="#6c757d">Octet 4</text>
  
  <!-- Network vs Host division -->
  <text x="50" y="300" font-family="Arial, sans-serif" font-size="16" font-weight="bold" fill="#495057">Network and Host Address Division:</text>
  
  <!-- Network portion -->
  <rect x="50" y="320" width="350" height="80" fill="#cce5ff" stroke="#0066cc" stroke-width="3" rx="5"/>
  <text x="225" y="340" text-anchor="middle" font-family="Arial, sans-serif" font-size="14" font-weight="bold" fill="#003d7a">Network Address</text>
  <text x="225" y="365" text-anchor="middle" font-family="Courier New, monospace" font-size="18" font-weight="bold" fill="#0066cc">192.168.123</text>
  <text x="225" y="385" text-anchor="middle" font-family="Arial, sans-serif" font-size="12" fill="#6c757d">Identifies the network</text>
  
  <!-- Host portion -->
  <rect x="420" y="320" width="150" height="80" fill="#ffe6cc" stroke="#ff6600" stroke-width="3" rx="5"/>
  <text x="495" y="340" text-anchor="middle" font-family="Arial, sans-serif" font-size="14" font-weight="bold" fill="#cc4400">Host Address</text>
  <text x="495" y="365" text-anchor="middle" font-family="Courier New, monospace" font-size="18" font-weight="bold" fill="#ff6600">132</text>
  <text x="495" y="385" text-anchor="middle" font-family="Arial, sans-serif" font-size="12" fill="#6c757d">Identifies the device</text>
  
  <!-- Full breakdown -->
  <text x="50" y="440" font-family="Arial, sans-serif" font-size="16" font-weight="bold" fill="#495057">Complete Address Breakdown:</text>
  
  <!-- Network address line -->
  <rect x="50" y="460" width="300" height="30" fill="#e6f3ff" stroke="#0066cc" stroke-width="1" rx="3"/>
  <text x="70" y="480" font-family="Arial, sans-serif" font-size="14" font-weight="bold" fill="#0066cc">Network Address:</text>
  <text x="200" y="480" font-family="Courier New, monospace" font-size="14" font-weight="bold" fill="#003d7a">192.168.123.0</text>
  
  <!-- Host address line -->
  <rect x="50" y="500" width="300" height="30" fill="#fff3e6" stroke="#ff6600" stroke-width="1" rx="3"/>
  <text x="70" y="520" font-family="Arial, sans-serif" font-size="14" font-weight="bold" fill="#ff6600">Host Address:</text>
  <text x="200" y="520" font-family="Courier New, monospace" font-size="14" font-weight="bold" fill="#cc4400">0.0.0.132</text>
  
  <!-- Router explanation -->
  <rect x="400" y="450" width="350" height="100" fill="#f8f9fa" stroke="#dee2e6" stroke-width="1" rx="5"/>
  <text x="575" y="470" text-anchor="middle" font-family="Arial, sans-serif" font-size="14" font-weight="bold" fill="#495057">How Routers Use This:</text>
  <text x="420" y="490" font-family="Arial, sans-serif" font-size="12" fill="#6c757d">• Routers use network address to</text>
  <text x="420" y="505" font-family="Arial, sans-serif" font-size="12" fill="#6c757d">  find the correct network</text>
  <text x="420" y="520" font-family="Arial, sans-serif" font-size="12" fill="#6c757d">• Final router delivers to specific</text>
  <text x="420" y="535" font-family="Arial, sans-serif" font-size="12" fill="#6c757d">  host using host address</text>
  
  <!-- Key point -->
  <rect x="50" y="560" width="700" height="30" fill="#d4edda" stroke="#28a745" stroke-width="2" rx="5"/>
  <text x="400" y="580" text-anchor="middle" font-family="Arial, sans-serif" font-size="14" font-weight="bold" fill="#155724">🔑 Key Point: IP = Network Part + Host Part (determined by subnet mask)</text>
</svg>

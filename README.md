## Netpractice 42 :

This project in mainly teaching the basics of networking. 

## What is a computer network?

A computer network is a bunch of devices connected together to exchange information — emails, documents, audio/video data — or to share a resource — printers, storages and other physical devices.

Typically, computers in a network are called **hosts**, while links are the elements that connect them. The picture below displays a very primitive form of network where two hosts are linked together through a physical cable.
![lan-network-with-two-computers-flat-vector-illustration-on-white-background-mapb2p](https://github.com/user-attachments/assets/1eec0e67-4255-402b-b15b-4bff8514acf5)
1. Two computers connected together via cable. This is the simplest form of computer network.

## What is the Internet Protocol Suite, also known as the TCP/IP protocol ?

The Internet Protocol Suite is a collection of protocols — that's what the word suite stands for — that determines how the Internet should work.

The TCP/IP alias comes from two of the most important protocols the Internet Protocol Suite contains:

the **Transmission Control Protocol (TCP)** and the **Internet Protocol (IP)**.

Initially developed by the United States Department of Defense and now maintained by the Internet Engineering Task Force (IETF), the TCP/IP protocol stack defines how data should be handled, transmitted, routed, and received over the Internet.

Anything that is connected to the Internet or operates with it must comply with the rules defined in the TCP/IP protocol stack.

Two machines that want to communicate over the Internet must both implement the TCP/IP protocol stack in order to talk to eachother correctly.

**For example**, the web browser you are using to read this article implements the **Hypertext Transfer Protocol (HTTP)**, one of the many protocols in the TCP/IP protocol stack and the foundation of the World Wide Web (WWW).

The HTTP protocol determines how the text you are reading right now should be sent from the web server — the remote computer that stores the information — to your web browser, over the Internet.

The protocol also describes how your browser should talk to the web server in order to initiate the data exchange.

Many other software parts must be TCP/IP compliant.

**For example**, the operating system running on your device has to implement several protocols from the TCP/IP suite, in order to provide Internet capabilities to the entire system (web browser included!).

## TCP/IP is about the software side of things

You won't find instructions on how to build networks, how signals should travel through cables and so on: the TCP/IP protocol stack is designed to be hardware independent and may be implemented on top of any physical technology.

**For example**, some IETF engineers during the April Fool's day designed the IP over Avian Carriers (IPoAC): a proposal to carry Internet traffic by birds such as homing pigeons.

## Anatomy of the TCP/IP protocol stack 

Cables and computers that make up the Internet infrastructure understand a very simple binary language made of zeroes and ones, and yet we want to be able to move rich data around such as web pages, emails, movies, video calls, … in a reliable, error-free and easy to establish way. 

This is a complex problem that must be broken down into smaller pieces to be solved efficiently. For this reason, the TCP/IP protocol stack has been organized into four layers.

Each layer contains protocols that describe how to route/transmit/receive data according to a different level of abstraction.

The lower the layer, the closer you are to the hardware and the more detailed the instructions are; the higher the layer, the closer you are to the human and the more abstract the communication becomes. Let's take a bottom-up look:

**1. Link layer** — also known as the physical layer, it contains protocols that operate very close to the metal. Protocols in this layer see the network as a bunch of machines physically linked together that exchange bits of data;

**2. Network layer**— also known as the Internet layer, this is where the communication starts to get fancy. Protocols in this layer think in terms of source networks and destination networks and how to identify them;

**3. Transport layer** — here the communication becomes even more abstract. Protocols in this layer think in terms of processes that talk to eachother through specific channels;

**4. Application layer** — the most abstract layer, where protocols think in terms of user services that exchange application data over the network.

<center><img width="262" height="440" alt="tcp-ip-stack" src="https://github.com/user-attachments/assets/b0d7a3c0-661a-4c1b-ab40-99c0c268f34b" /></center>
<center>1. The four layers of the TCP/IP protocol stack.</center>

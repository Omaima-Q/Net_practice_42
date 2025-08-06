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


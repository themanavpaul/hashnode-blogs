---
title: "What happens when you search 8.8.8.8 dns?"
seoTitle: "Google Search Process Explained"
seoDescription: "Explore the journey of data from browser to server when you type "www.google.com" and uncover network concepts at play"
datePublished: Wed Oct 30 2024 10:41:04 GMT+0000 (Coordinated Universal Time)
cuid: cm2vqxmeo000a09jwfquqa0bu
slug: what-happens-when-you-search-8888-dns
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1730261014085/52214c79-b91f-4045-a490-5f5db08f7a51.png
tags: google, devops, 30-days-of-code, computer-networking, ip-address, wemakedevs, 100xdevs

---

Have you ever wondered what happens when you type "www.google.com" into your browser’s url bar and hit enter? It seems like magic, right? Information instantly appears on your screen, but behind the scenes, there's a fascinating dance of computers, protocols, and data packets happening at lightning speed. Today, we'll embark on a journey to unravel this digital mystery and explore the fundamental concepts of computer networks!

**The Cast of Characters:**

* **Client:** Think of this as the initiator, like your web browser. It sends requests for information.
    
* **Protocol:** Imagine this as a secret handshake. Protocols are sets of rules that govern how data is exchanged between devices.
    
* **Data Packet:** Data doesn't travel in one big chunk, it's broken down into smaller, easier-to-manage pieces called packets.
    
* **Server:** This is the responder, like a giant warehouse full of information. It processes requests and sends back the data you need.
    
* **Web Server:** A specialized server that speaks the language of the web – HTTP (Hypertext Transfer Protocol).
    

---

**The IP Address Mystery:**

Every device on a network has a unique identifier called an IP Address. Think of it like a house address on the internet. Here's an example:

* [**I**](https://www.google.com/url?sa=E&source=gmail&q=https://www.google.com)**P Address:** `8.8.8.8` (This one actually belongs to Google's public DNS server!)
    
* **IPv4:** The most common version, using 32 bits to represent an address. Example: `192.168.1.100`
    
* **IPv6:** A newer version using 128 bits, providing a much larger address space. Example: `2001:0db8:85a3:0000:0000:8a2e:0370:7334`
    

**Port Numbers : The Specific Doors on Your Network Device**

Imagine your computer as a building. Each room within that building is like a different application or service running on your computer. To access a specific room, you need to know the room number or identifier. Similarly, on your computer, each application or service has a unique identifier called a port number.

A **port number** is like a specific door on your computer. It tells incoming data packets which application or service they should be directed to. Think of it as the room number for a particular service running on your computer.

* **Well-Known Ports (0-1023):** Reserved for specific services. Examples:
    
    * **Port 80:** HTTP (Hypertext Transfer Protocol)
        
    * **Port 443:** HTTPS (Secure Hypertext Transfer Protocol)
        
    * **Port 22:** SSH (Secure Shell)
        
    * **Port 25:** SMTP (Simple Mail Transfer Protocol)
        
* **Registered Ports (1024-49151):** Assigned by the Internet Assigned Numbers Authority (IANA) for specific applications.
    
* **Ephemeral Ports (49152-65535):** Used by applications for temporary connections.
    

**Example:**

If you want to access a web server on a computer with the IP address 192.168.1.100, you would typically use port 80. So, the complete address would be:

* `http://192.168.1.100:80`
    

This tells your browser to connect to the web server on that IP address using port 80, which is the standard port for HTTP.

---

**But How Does Your Computer Know That 8.8.8.8 is Google's Server?**

Here's where the magic of DNS (Domain Name System) comes in! Just like a phone book helps you find a name by its phone number, DNS translates human-friendly domain names (like google.com) into their corresponding IP addresses.

**The DNS Dance:**

1. **The Request:** Your browser (the client) sends a request for "www.google.com" to your internet service provider (ISP), like Airtel or Jio.
    
2. **Calling the DNS Resolver:** Your ISP has a built-in DNS resolver, which acts like a phone book lookup service.
    
3. **A Chain of Servers:** If it's a new website for you, the resolver might start at the root name servers and then move down through the chain of servers responsible for different parts of the domain name (like ".com").
    
4. **Finding the Right Server:** Eventually, it reaches the specific server (like Amazon Route 53) responsible for "google.com" and asks, "Hey, what's the IP address for this domain?"
    
5. **The Answer Arrives:** The server responds with the IP address (e.g., 142.250.194.142).
    
6. **Back to You:** The IP address is sent back through your ISP's resolver and finally reaches your browser.
    

**Caching for Speed:**

To avoid this whole DNS lookup every time you visit the same website, your computer and your ISP might cache the IP address for a while, making future visits much faster.

**Setting Up the Connection:**

Now that your browser has the IP address, it can finally connect to the server. But there's one more step! TCP (Transmission Control Protocol) uses a three-way handshake to establish a reliable connection. Imagine it like a secret knock to confirm it's the right person before opening the door.

To initiate a connection, TCP uses a three-way handshake:

1. **Client → SYN → Server:** Your browser (the client) sends a SYN (synchronize) packet to the server, indicating its desire to establish a connection.
    
2. **Client ← SYN ACK ← Server:** The server responds with a SYN-ACK (synchronize acknowledge) packet, acknowledging the client's request and proposing a sequence number for the connection.
    
3. **Client → ACK → Server:** The client sends an ACK (acknowledge) packet back to the server, confirming the sequence number and establishing the connection.
    

Once the handshake is complete, a reliable connection is established between the client and the server, and data can start flowing.

**The Language of the Web:**

Once connected, your browser speaks the language of the web – HTTP (Hypertext Transfer Protocol). It sends a request for the specific information you're looking for (like the Google homepage).

**The Server Responds:**

The server processes the request and sends back the data, usually in the form of HTML, CSS, and JavaScript files.

**Your Browser Takes Over:**

Finally, your browser receives the data, interprets it using its engine, and renders the beautiful website you see on your screen.

---

Phew! That was quite a journey, wasn't it? All of this happens in a fraction of a second while you patiently (or impatiently!) wait for your search results.

But this is just the tip of the iceberg. There's a whole world of networking concepts waiting to be explored.

**▶ Next → Generative AI from Zero to Hero in 30 Days.**

👨🏻‍💻 Connect with me on [LinkedIn](https://www.linkedin.com/in/manav-paul/) and [X](https://x.com/themanavpaul)(Twitter).
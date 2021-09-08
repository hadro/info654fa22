This page intentionally left blank. ⬇️, ➡️, or spacebar 🛰 to start slidedeck.
---
class: center, middle

# Welcome to Class 2!


---

# Agenda

- Assignment questions?
- News of the Week
- Imperfect metaphor of the week
- Readings
- Break!
- How the Internet Works!
  - Servers and DNS
	- URL and URIs
  - HTTP Status codes
  - TCP/IP
- Break!
- Wireshark demo (Hacking, monitoring, and what users do with these networks)
- Network Inspection (Chrome/Firefox tool)

---

## Assignment questions?

---

## News of the Week

Drop a link on the etherpad:
<https://etherpad.wikimedia.org/p/prattsi654fa21-2>

---
class: center, middle

#Imperfect metaphor of the week
---
background-image: url(https://ephemeralnewyork.files.wordpress.com/2009/06/crotonreservoir.jpg)

--
background-image: url(https://archive.li/bfmtJ/abc9fdf8bd33f02eafb6d907f90c4b140492ca2e.jpg)

---
background-image: url(https://web.archive.org/web/20050215063331im_/http://mindfully.org:80/Water/2004/NYC-Store-Water16may04f3.gif)
---
background-image: url(https://imgs.6sqft.com/wp-content/uploads/2016/03/10190245/nyc-water-supply-system1.jpg)

---

class: middle, center

# Readings

--

Thoughts? Reactions? Suprises?

---
class: center, middle

# Networks

--

[Original [info + slides by Ashley Blewer](https://training.ashleyblewer.com/presentations/networks.html)]

---
# Networks

- protocols
- infrastructure
- the Internet

---

## But first

--

I want you to stare at the bottom left corner of your web browser, then hit refresh.
Do this a couple of times.

--

What do you see when you do this?

---
# Networks

A network is two or more devices that are connected together, and are able to communicate or share resources with each other. I like this picture because the firewall is on fire for some reason.

.center[![network-fire](./img/network-fire.png)]

---
## Never forget

... this all literally started as a sci-fi dream:

--

## **`"Galactic Network"`**


---

# What is the Internet?

> "Internet" refers to the global information system that -- (i) is logically linked together by a globally unique address space based on the Internet Protocol (IP) or its subsequent extensions/follow-ons; (ii) is able to support communications using the Transmission Control Protocol/Internet Protocol (TCP/IP) suite or its subsequent extensions/follow-ons, and/or other IP-compatible protocols; and (iii) provides, uses or makes accessible, either publicly or privately, high level services layered on the communications and related infrastructure described herein

---

## What's the difference between:
- "The Internet"
- "The World Wide Web"

?

---
# Protocols

This communication can happen because of established rules and standards around the sending of data.

--

## What are some examples of protocols you may have come across?

--

Shout 'em out!

---


Some common protocols for networking are:

- TCP/IP
- FTP (sending files)
- SMTP (email)
- HTTP
- Wi-Fi
- Bluetooth
- LTE


---
<!--
![](./img/reabracadabra.jpg)

- [source: Rhizome Net Art Anthology: Reabracadabra](https://anthology.rhizome.org/reabracadabra)
- [wikipedia page on the Minitel](https://en.wikipedia.org/wiki/Minitel)

--- -->

![network protocols](./img/b0rk-network-protocols.jpeg)

- [source](https://twitter.com/b0rk/status/1222273122986024961)
---

# TCP/IP

**TCP**: Transmission Control Protocol  
**IP**: Internet Protocol

![](./img/survived-tcp.jpg)

---
# TCP/IP
It is a set of rules that govern how data is transferred over the internet.  

TCP/IP was standardized via the [Internet Engineering Task Force](https://www.ietf.org/), and in fact the organization itself was established in order to properly identify and formalize TCP/IP as a standard.

---
# Introduction to TCP/IP

The 4-Layer Model (4m32s)

<iframe width="560" height="315" src="https://www.youtube.com/embed/KEWe-5Bk3Q0"
frameborder="0"
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

---
# The 4 layers

- Application layer (sends information to transport layer)
- Transport (TCP) layer (breaks packets down, ensures reliable byte stream)
- Internet (IP) layer (pair each packet to proper IP destination)
- Link layer (sends packets between IP and hosts)

---
# HTTP, FTP, SMTP

These are all internet protocols that work at the application level to help you access websites (HTTP), send files (FTP) and send email (SMTP) over the network.  

![](./img/computer_e-mail.gif) ![](./img/computer_e-mail.gif) ![](./img/computer_e-mail.gif)

---
# HTTPS?

HTTPS is a protocol developed on top of HTTP that takes extra steps to ensure security, privacy, and integrity of the communication channel between you and the website.  

![](./img/computerhorsepics.gif)

Why is this such a big deal?

---
# Activity: 🐠 Test your network 🦈

Use [WireShark](https://www.wireshark.org/) to understand your surroundings.

What is WireShark?  

> "Wireshark is the world’s foremost and widely-used network protocol analyzer. It lets you see what’s happening on your network at a microscopic level and is the de facto (and often de jure) standard across many commercial and non-profit enterprises, government agencies, and educational institutions." [source: website](https://www.wireshark.org/)

---
# Wireshark non-live demo

[HakTip - How to Capture Packets with Wireshark - Getting Started](https://www.youtube.com/watch?v=6X5TwvGXHP0)

<iframe width="560" height="315" src="https://www.youtube.com/embed/6X5TwvGXHP0" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

---

# IP Addresses
## (The "IP" part of TCP/IP)

This is an IP Address:

<http://173.194.221.139>

--

Computers can understand it ...

humans not so much.

---

IPv4 (Internet Protocol version 4)  

32 bit  

4,294,967,296 possible addresses (2^32, or 256 \* 256 \* 256 \* 256)

Why is this a problem?

---
Enter IPv6

128-bit address

... or approximately 3.4×10^38 addresses

---
## So how do humans engage with this IP system effectively?


---
# Distributed Name Service (DNS)

What does this do?

.center[![](./img/dnsbutton.gif)]

---
# Distributed Name Service (DNS)

- gives human-readable names to IP addresses
- lets people have simple email addresses
- gives us domain names (.com, .net, .club)

.center[![](./img/dnsbs.gif)]


---

## Uniform Resource Locators (URLs)

--

In meta-description:

#### `scheme://subdomain.domain.TopLevelDomain:port/path?query_string#fragment_id`

--
E.g.

<https://iiif.io/event/2020/iiifweek/#monday-june-1st>

--

<https://www.theatlantic.com/magazine/archive/1945/07/as-we-may-think/303881/?single_page=true>


---

## What are some of the most common TLDs?

--

## What are other more exotic TLD options?


---

# HTTP Status codes

HTTP status codes are how our browsers know whether resources are where the URL says they should be.

--

They handle a variety of critical scenarios:
- Resources have changed addresses (think: automatic redirects)
- A user doesn't have permission to see a certain resources (think: pages that require login)
- A server is unable to deliver the resource, even though the address is accurate (think: someone's site is down entirely)

---

## HTTP status codes come in "series"
- 200 series
- 30x series
- 40x series
- 50x series

---

## OK 200

The request was fulfilled

--

> Note: you'll basically never actually "see" this code in the application layer -- it means the request worked as expected!

---

## Redirection 3xx

E.g., 301 redirect means "Moved permanently"

http://si.pratt.edu

TO

https://www.pratt.edu/academics/information/


---

## Then there are the errors:
- USER ERRORS (400 series)
- SERVER ERRORS (500 series)

---

## Unauthorized 401
--

## Forbidden 403
--

## Not found 404

--

![](https://i.imgur.com/9Es6Z82.gif)

---

## 500 Internal Server Error

---

## https://httpstatusdogs.com/
## https://http.cat/

--
<img src="https://http.cat/401" width="70%" />

---

<img src="https://httpstatusdogs.com/img/301.jpg" width="70%" />

---


<https://twitter.com/DanaDanger/status/183316183494311936>


<pre>HTTP response codes for dummies.
50x: we screwed up.
40x: you screwed up.
30x: ask that dude over there.
20x: cool.</pre>


---
class: center, middle

# The Internet

"The best-known computer network"

![map-of-internet](./img/map-of-internet.png)

[source](http://www.opte.org/maps/)

---
# The Internet

- [Quartz: Map of the Internet](https://qz.com/se/map-of-the-internet/)

- size and scope
- built up of things

---
# The internet is a real place

- Data centers
- Cables
- Towers
- Satellites
- in the air around us right now


---
# Submarine cables

Large networked systems are connected to each other via undersea cables.

.center[![submarine-cables](./img/submarine-cables.png)]

[source: submarinecablemap.com](https://www.submarinecablemap.com/)

---
# Is this a lot?

.center[![eye-martini](./img/eye-martini.gif)]

Almost done!

---
# People make networks

Not everything has to be super technical, there is a very large and chaotic "people" layer when it comes to computer networks.

.center[![dollz](./img/dollz.gif)]

---

# Network Inspection (Chrome/Firefox tool)

Press option+command+I (on a Mac or PC, in Chrome or in Firefox)

---
# Moment of zen

[Simon Weckert: Google Maps Hacks (2020)](http://www.simonweckert.com/googlemapshacks.html)

<iframe width="560" height="315" src="https://www.youtube.com/embed/k5eL_al_m7Q" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

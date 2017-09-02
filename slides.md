dhcpcanon
=========

DHCP client disclosing less identifying information.

https://github.com/dhcpap

PrototypeFund demo day, Berlin, 31st August 2017

----  ----

What is DHCP
=============

----

Dynamic Host Configuration Protocol (DHCP)
-------------------------------------------
- network protocol to get IP addresses and networking parameters automatically
- transparent to the end user
- user interact with a network manager

----

Local network image
---------------------

![image](images/serveimage.png)

----

DHCP session
--------------

![image](images/DHCP_session.svg)<!-- .element:  style="width: 30%; float:left" -->

1. my laptop: can i have an address?<!-- .element: class="fragment" data-fragment-index="0" -->
2. server:    i can offer you 192.168.1.23<!-- .element: class="fragment" data-fragment-index="1" -->
3. my laptop: i request 192.168.1.23<!-- .element: class="fragment" data-fragment-index="2" -->
4. server:    assigned to you!<!-- .element: class="fragment" data-fragment-index="3" -->

----

DHCP session, detailed
-----------------------

1. my laptop: can i have an address?<!-- .element: class="fragment" data-fragment-index="0" -->
  * btw my laptop name is juga_laptop<!-- .element: class="fragment" data-fragment-index="1" -->
  * it's a Dell i bought in Copenhague in 2013<!-- .element: class="fragment" data-fragment-index="2" -->
  * i use Debian with dhclient version 4.3.5<!-- .element: class="fragment" data-fragment-index="3" -->
  * i like the coffee with milk<!-- .element: class="fragment" data-fragment-index="4" -->
2. server:    i can offer you 192.168.1.23<!-- .element: class="fragment" data-fragment-index="5" -->
  * btw, you can find milk in the fridge<!-- .element: class="fragment" data-fragment-index="6" -->

----  ----

Issues with DHCP
=================

- reveal identifying information
- new standard to minimize it (RFC 7844)
- only a Windows 10 implementation

![image](images/Windows_darkblue_2012_svg.svg)<!-- .element:  style="width: 40%;" -->

----  ----

What I had before
==================

![image](images/Python_logo_and_wordmark.svg)<!-- .element:  style="width: 40%;" -->

- ``dhcpcanon``:
  a prototype Python DHCP client implementing part of the protocol
- ideas on how to further develop it

----  ----

Achieved
=========

----

``dhcpcanon``
---------------
- decisions on what and how to implement:
  follow Windows 10 implementation instead of restricted version of RFC 7844
- complete the protocol
- automatic testing
- improve documentation
- Debian package
- contact with different Linux distributions to test it


----

Example Windows 10 capture
---------------------------

![image](images/dhcp_win_req_renew_mac_annotated.svg)

----

Example ``dhclient`` capture
------------------------------

![image](images/dhcp_dhclient_req_renew_mac_annotated.svg)

----

``systemd`` (system manager)
-----------------------------

- modified DHCP client code to enable Anonymity Profiles
- code in the process of being merge by ``systemd`` team

----

``Gnome Network Manager`` (network manager)
---------------------------------------------

Developing a proper integration in process

----

``dhcpcfp``
------------

A network scanner to show:
- which is the identifying information can be found
- how is different to the Anonymity profiles
- how operating system, device and/or person can be guessed

----

Internet Engineering Task Force meeting
------------------------------------------
![image](images/IETF_Logo.svg)<!-- .element:  style="width: 20%;" -->

[IETF](https://ietf.org/meeting/99/index.html)
- suggestions from the main author of the RFC 7844

----

Bornhack hacker camp
----------------------
![image](images/bornhack-2017-logo-s.jpg)<!-- .element:  style="width: 40%;" -->

[Bornhack](https://bornhack.dk/bornhack-2017/program/#/event/get-ip-addresses-without-leaking-identifying-information)  
- presentation: feedback and interesting ideas
- workshop: catch bugs

----

Linux distribution communities
---------------------------------

Interest on integrating ``dhcpcanon``: Debian, Tails, Subgraph, Gentoo, Archlinux

![image](images/openlogo-nd.svg)<!-- .element:  style="width: 10%;" -->
 ![image](images/Tails-logo-flat-inverted.svg)<!-- .element:  style="width: 20%;" -->
 ![image](images/Subgraph_OS_Logo.png)<!-- .element:  style="width: 20%;" --> ![image](images/Gentoo_Linux_logo_matte.svg)<!-- .element:  style="width: 10%;" -->
 ![image](images/Arch_Linux_logo.svg)<!-- .element:  style="width: 20%;" -->

----  ----

Learned
=====================

----

Worth to remember
-----------------
- *release early, release often*
- *divide and conquer* (on tasks)
- is fun and productive to work with others
- challenging to explain technical concepts to non technical users

----

New
------

- present earlier to get feedback and bug reports earlier
- strategies to develop awareness (thanks marketing coaching!!)

----

IETF community
---------------

- worldwide open standards organization
- anyone can participate
- though difficult without funding nor corporate sponsor
- *rough consensus and working code*

----

Internet protocols development
---------------------------------

- political and historical reasons
- how the need for the Anonymity Profiles actually happens

![image](images/InternetProtocolStack.png)<!-- .element:  style="width: 20%;" -->

----

DHCP fingerprint databases
----------------------------

![image](images/fingerbank_dhclient_screenshot.png)

----  ----

Did not work as planned
==============================

- planning :(
- the protocol and integration with operating systems
  can be more complex than i knew or expected

----  ----

What is next
=============

----

dhcpcanon, systemd
---------------------

- more people to test it to be ready for end users
- further development (IPv6)
- further operating systems compatibility (WIP)
- further documentation

----

Others
-------

- domain and Web page to facilitate finding documentation (WIP)
- final report
- more presentations and/or worshops
- Raspberry Pi image for demonstration purposes

![image](images/Raspberry_Pi_Logo.svg)<!-- .element:  style="width: 150px;" -->

----

Other operating systems implementations
----------------------------------------

![image](images/Android_robot_2014.svg)<!-- .element:  style="width: 150px;" -->
 ![image](images/Freebsd_logo.svg)
 ![image](images/Apple_logo_black.svg)

Android, FreeBSD, Mac OS, iOS...


----  ----

Thank you very much!
======================

Many people for their very valuable ideas and suggestions.

Excelent PrototypeFund team :-)


![image](images/prototypefund_square.jpg)<!-- .element:  style="width: 10%;" -->
 ![image](images/sprite.svg.svg-logo-en.png)<!-- .element:  style="width: 10%;" -->

----  ----

Contact
==========

![image](images/juga_qr.svg)

juga at riseup dot net

2DA8 1D01 455C 3A00 3219  8850 F305 447A F806 D46B

IRC: #dhcpcanon at havana.baconsvin.org:6697

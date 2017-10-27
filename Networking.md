# Networking
This page provides resources and information for working with the computer networking aspect of the FRC robot.

## The network on the robot
The robot can be connected into a network in a number of ways.  In the following diagrams, `----` indicates an Ethernet cable, while `))))` represents a WiFi connection.

On the field, the network looks something like:
````
[Driver laptop]------[field network]  )))))  [Robot radio]------[RoboRIO]
````

In wireless practice (typically during build and preseason), the network looks something like:
````
[Driver laptop]  ((((  [Robot radio]------[RoboRIO]
````
In this configuration, the robot radio is configured as an access point, and the laptop initiates a connection to it.

In tethered practice (used in the Pits), we connect an Ethernet cable to the radio:
````
[Driver laptop]----[Robot radio]------[RoboRIO]
````

## IP addresses
Every network interface in our networks has an IP [(Internet Protocol](https://en.wikipedia.org/wiki/Internet_Protocol)) address.  You can think of this like the address of a house.  In almost all cases where two computers need to exchange information, the sender transmits packets addressed to the IP address of the destination.

Unlike home addresses, computers often change their IP addresses.  Typically when a computer first connects to a network, it asks the network for an IP address, using a method called DHCP [(Dynamic Host configuration Protocol](https://en.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol)).  In a typical network, one machine (the DHCP server) is configured to assign new computers their IP addresses.
	- During a match, this computer is in the field control network
	- During wireless or tethered practice, this computer is the robot radio

IP addresses take on one of two formats:
	- IPv4 addresses are 4 decimal integers between 0 and 255 separated by a dot, such as:
		- `10.0.95.2` (the typical roboRIO address)
		- `8.8.8.8`
		- `192.168.1.20` 
	- IPv6 addresses are up to 8 groups of 4-digit [hexadecimal](https://en.wikipedia.org/wiki/Hexadecimal) integers separated by colons, such as:
		- `2001:0db8:0000:0042:0000:8a2e:0370:7334`
		- `2001:db8::ff00:42:8329` (shorthand for `2001:0db8:0000:0000:0000:ff00:0042:8329`)

## The Domain Name System
Many people go their whole lives without knowing about IP addresses, because of a mechanism that prevents people and computers from needing to learn and remember the IP address of each computer.  When you type `google.com` into your web browser, your operating system queries a local [DNS](https://en.wikipedia.org/wiki/Domain_Name_System) server.  The server then provides the IP address for `google.com`.  

None of the robot networks include a DNS server.  Instead, a similar system called [mDNS](https://en.wikipedia.org/wiki/Multicast_DNS) is used.  Rather than ending in .com etc, mDNS addresses will typically end in .lan for IPv4, or .local for IPv6.

## Useful tools
- `ping` is a command on Windows, Mac, and Linux that will test communications with another computer.
	- Just type `ping google.com` and see what happens.  If it doesn't stop, press control-C.
	- Sometimes computers are configured not to respond to pings.
- `nslookup` is a command to ask a DNS server for the IP address of a computer.
	- Just type `nslookup google.com` and see what happens.
- To see your computer's IP address, type `ipconfig` on Windows or `ifconfig` on Mac and Linux.
- To request an IP address from the nearest DHCP server:
	- On Windows, type `ipconfig /renew`
	- On Linux, type `sudo dhclient`
- [Wireshark](https://www.wireshark.org/download.html) is a tool that shows traffic on an Ethernet or WiFi interface
	- With this tool, you can see the packets that compose various network conversations.  
	- Wireshark will do some basic breakdown of each packet into its [layers](https://en.wikipedia.org/wiki/OSI_model#Examples), explaining their meaning as much as it can.
- PuTTY, a Windows desktop client for the Secure SHell (SSH) remote access protocol, to configure and debug the robot
	- Download it here: https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html
	- The website has a rather '90s vintage look to it, but remains one of the top SSH clients for Windows
- FileZilla, a Windows desktop client for the Secure File Transfer Protocol (SFTP), to access files store on the robot
	- Download it here: https://filezilla-project.org/download.php

## Useful tricks
### Setting a static IP address on a Windows machine
TODO
### Finding the IP address of a computer that isn't otherwise responding
TODO
# Networking
This repository contains a computer networking simulation built using Cisco Packet Tracer. The project demonstrates the design, configuration, and implementation of a network across three company branches, focusing on connectivity, routing, and communication.

Here is how each branch was configured using the cisco packet tracer:
Router>enable  (User Mode)
Router#Configure Terminal (Privilege Mode)
Router(config)#           (Global Mode)
Router(config)#hostname VEPHLA-LAGOS  
VEPHLA-LAGOS(config)# banner motd @
THIS IS VEPHLA LAGOS NETWORK, INTRUDERS STAY OFF @

VEPHLA-LAGOS(config)#
VEPHLA-LAGOS(config)#enable secret Vephla12345
VEPHLA-LAGOS(config)#line console 0
VEPHLA-LAGOS(config-line)#password Vephla1234
VEPHLA-LAGOS(config-line)#login

VEPHLA-LAGOS(config-line)#line vty 0 4
VEPHLA-LAGOS(config-line)#password Vephla123
VEPHLA-LAGOS(config-line)#login
VEPHLA-LAGOS(config-line)#exit

VEPHLA-LAGOS(config#int f0/0
VEPHLA-LAGOS(config-if)#ip address 192.169.10.1 255.255.255.224
VEPHLA-LAGOS(config-if)#no shutdown

VEPHLA-LAGOS(config-if)#into s0/0
VEPHLA-LAGOS(config-if)#ip address 192.169.10.33 255.255.255.224
VEPHLA-LAGOS(config-If)#no shut
VEPHLA-LAGOS(config-If)#description Router Link Port connecting to KADUNA SERIAL 0 PORT
VEPHLA-LAGOS(config-If)#end

VEPHLA-LAGOS#copy run start or write (To save what you've configured. And you have to click on enter twice)

VEPHLA-LAGOS#show run  (Shows what you've configured or what is currently running on the router).
VEPHLA-LAGOS#show start (Shows what you've saved on the router).

It is on the Privilege Mode... we Test connectivity, we troubleshoot etc.



First router
enable secret - lagos54321
line console - lagos5432
vty - lagos543

Second router
enable secret - abuja54321
line console - abuja5432
vty - abuja543

Third router
enable secret - kaduna54321
line console - kaduna5432
vty - kaduna543


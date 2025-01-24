# Networking

This repository contains a computer networking simulation built using Cisco Packet Tracer. The project demonstrates the design, configuration, and implementation of a network across three company branches, focusing on connectivity, routing, and communication.

## Branch Configuration

Here is how each branch was configured using Cisco Packet Tracer:

### Router Configuration

```plaintext
Router>enable  (User Mode)
Router#configure terminal (Privilege Mode)
Router(config)#           (Global Mode)
Router(config)#hostname VEPHLA-LAGOS
VEPHLA-LAGOS(config)#banner motd @
THIS IS VEPHLA LAGOS NETWORK, INTRUDERS STAY OFF @

VEPHLA-LAGOS(config)#enable secret Vephla12345
VEPHLA-LAGOS(config)#line console 0
VEPHLA-LAGOS(config-line)#password Vephla1234
VEPHLA-LAGOS(config-line)#login

VEPHLA-LAGOS(config-line)#line vty 0 4
VEPHLA-LAGOS(config-line)#password Vephla123
VEPHLA-LAGOS(config-line)#login
VEPHLA-LAGOS(config-line)#exit

#Interface Configuration

VEPHLA-LAGOS(config)#interface f0/0
VEPHLA-LAGOS(config-if)#ip address 192.169.10.1 255.255.255.224
VEPHLA-LAGOS(config-if)#no shutdown

VEPHLA-LAGOS(config)#interface s0/0
VEPHLA-LAGOS(config-if)#ip address 192.169.10.33 255.255.255.224
VEPHLA-LAGOS(config-if)#no shutdown
VEPHLA-LAGOS(config-if)#description Router Link Port connecting to KADUNA SERIAL 0 PORT
VEPHLA-LAGOS(config-if)#end

#Saving and Viewing Configurations

VEPHLA-LAGOS#copy run start or write
(To save what you've configured. Press Enter twice.)

VEPHLA-LAGOS#show run
(Shows what you've configured or what is currently running on the router.)

VEPHLA-LAGOS#show start
(Shows what you've saved on the router.)

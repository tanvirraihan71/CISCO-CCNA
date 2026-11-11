Here are all the commands from the note:

Mode navigation

enable
configure terminal      (conf t)
interface gi0/1
exit
end                     (or Ctrl+Z)
disable

Show commands

show running-config     (sh run)
show startup-config
show version
show ip interface brief
show interfaces
show interfaces status
show vlan brief
show mac address-table
show ip route
show arp
show cdp neighbors
show logging

Output filters

show running-config | include hostname
show running-config | section interface
show ip interface brief | include up

Basic configuration

hostname SW-CORE-01
enable secret MyStrongPass
service password-encryption
line console 0
password ConsolePass
login
logging synchronous
banner motd # Authorized access only #
interface vlan 1
ip address 192.168.1.10 255.255.255.0
no shutdown
description Management

SSH setup

ip domain-name mycompany.local
username admin secret AdminPass
crypto key generate rsa modulus 2048
ip ssh version 2
line vty 0 15
transport input ssh
login local

Save

copy running-config startup-config    (copy run start)
write memory

Undo / reset

no <command>
shutdown
no shutdown
default interface gi0/5
reload
reload in <minutes>

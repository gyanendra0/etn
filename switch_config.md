AIM: To configure a switch appropriately with required properties.

THEORY: The properties of a switch can be configured using CLI, short for Command Line Interface. 

There are several modes in the CLI and each mode is used to modify certain specific attributes of the switch.

 The modes of execution and their uses are listed in the table as under
 
 ![image](https://user-images.githubusercontent.com/56673648/146443629-26c33634-92b0-4c7b-8037-988bd0822a9d.png)

Topologies:

![image](https://user-images.githubusercontent.com/56673648/146444139-2e8e6965-e91c-4abc-bc4f-1d10072213a5.png)

![image](https://user-images.githubusercontent.com/56673648/146444177-36016b69-9d21-4b75-810c-c61f092720f9.png)

STAR TOPOLOGY

Switch>en

Switch#conf t

Enter configuration commands, one per line. End with CNTL/Z.

Switch(config)#no ip domain-lookup

Switch(config)#interface fa0/1

Switch(config-if)#shutdown



Switch(config-if)#

%LINK-5-CHANGED: Interface FastEthernet0/1, changed state to administratively down

%LINEPROTO-5-UPDOWN: Line protocol on Interface FastEthernet0/1, changed state to down

Switch(config-if)#interface fa0/1

Switch(config-if)#no shutdown

Switch(config-if)#

%LINK-5-CHANGED: Interface FastEthernet0/1, changed state to up

%LINEPROTO-5-UPDOWN: Line protocol on Interface FastEthernet0/1, changed state to up

Switch(config-if)#end

Switch#

%SYS-5-CONFIG_I: Configured from console by console

Switch#conf t

Enter configuration commands, one per line. End with CNTL/Z.

Switch(config)#enable secret class

Switch(config)#line con 0

Switch(config-line)#password 12345

Switch(config-line)#login

Switch(config-line)#end

Switch#

%SYS-5-CONFIG_I: Configured from console by console

Switch#show running-config

Building configuration...

Current configuration : 1172 bytes
!

version 15.0

no service timestamps log datetime msec

no service timestamps debug datetime msec

no service password-encryption

!

hostname Switch

!

enable secret 5 $1$mERr$9cTjUIEqNGurQiFU.ZeCi1

!

!

!

no ip domain-lookup

!

!

!

spanning-tree mode pvst

spanning-tree extend system-id

!

interface FastEthernet0/1

!

interface FastEthernet0/2

!

interface FastEthernet0/3

!

interface FastEthernet0/4

!

interface FastEthernet0/5

!

interface FastEthernet0/6

!

interface FastEthernet0/7

!

interface FastEthernet0/8

!

interface FastEthernet0/9

!

interface FastEthernet0/10

!

interface FastEthernet0/11

!

interface FastEthernet0/12

!

interface FastEthernet0/13

!

interface FastEthernet0/14

!

interface FastEthernet0/15

!

interface FastEthernet0/16

!

interface FastEthernet0/17

!

interface FastEthernet0/18

!

interface FastEthernet0/19

!

interface FastEthernet0/20

!

interface FastEthernet0/21

!

interface FastEthernet0/22

!

interface FastEthernet0/23

!

interface FastEthernet0/24

!

interface GigabitEthernet0/1

!

interface GigabitEthernet0/2

!

interface Vlan1

no ip address

shutdown

!

!

!

!

line con 0

password 12345

login

!

line vty 0 4

login

line vty 5 15

login

!

!

!

!

end



Switch#

Switch#conf t

Enter configuration commands, one per line. End with CNTL/Z.

Switch(config)#host Host1

Host1(config)#interface vlan1

Host1(config-if)#ip address 192.168.1.2 255.255.255.0

Host1(config-if)#no shut



Host1(config-if)#

%LINK-5-CHANGED: Interface Vlan1, changed state to up



%LINEPROTO-5-UPDOWN: Line protocol on Interface Vlan1, changed state to up



Host1(config-if)#end

Host1#

%SYS-5-CONFIG_I: Configured from console by console


Host1#copy run start

Destination filename [startup-config]? 

Building configuration...

[OK]

Host1#conf t

Enter configuration commands, one per line. End with CNTL/Z.

Host1(config)#line vty 0 15

Host1(config-line)#password 12345

Host1(config-line)#login

Host1(config-line)#banner motd #Hello!!#

Host1(config)#end

Host1#

%SYS-5-CONFIG_I: Configured from console by console



Host1#copy run start

Destination filename [startup-config]? 

Building configuration...

[OK]


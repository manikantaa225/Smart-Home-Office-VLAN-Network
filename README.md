# Smart-Home-Office-VLAN-Network
This project demonstrates the design and implementation of a Smart Home-Office Network using Cisco Packet Tracer. The network integrates VLANs, DHCP, SSH, and Inter-VLAN Routing (Router-on-a-Stick method) to ensure efficient communication and secure management.
## Project Overview
The objective of this project is to design a small-scale home-office hybrid network that:  <br>
Divides users into separate VLANs for logical segmentation.   <br>
Provides dynamic IP addressing using DHCP.   <br>
Allows secure remote access using SSH.    <br>
Enables communication between VLANs using Router-on-a-Stick.    <br>
Connects both wired and wireless devices (Laptops, PCs, Smartphones, Printers).    <br>

 ## Network Topology

The topology includes:     <br>
Router (1) – Configured with sub-interfaces for Inter-VLAN Routing.    <br>
Switch (1) – Central device for VLAN segmentation.      <br>
Access Points (3) – Wireless connectivity for smartphones & laptops.      <br>
End Devices – Laptops, PCs, Printers, Smartphones across VLANs.        <br>
Each VLAN represents a different department/zone:      <br>
VLAN 10 (Blue Zone) – Laptop0, Smartphone0, PC0, Printer0      <br>
VLAN 20 (Purple Zone) – Laptop1, Smartphone1, PC1, Printer1     <br>
VLAN 30 (Pink Zone) – Laptop2, Smartphone2, PC2, Printer2      <br>

<img width="1912" height="806" alt="Image" src="https://github.com/user-attachments/assets/14c4a966-bbfe-4cd8-b281-c029e9e9c3cb" />

 ## Configurations
## VLAN Configuration   <br>

VLAN 10, VLAN 20, VLAN 30 created on the switch.  <br>
Switch ports assigned to respective VLANs.  <br>
 
!       <br>
enable    <br>
configure terminal    <br>
 
vlan 10       <br>
 name VLAN10_HOME     <br>
vlan 20      <br>
 name VLAN20_OFFICE     <br>
vlan 30     <br>
 name VLAN30_GUEST      <br>
exit     <br>

Assign Ports to VLANs    <br>
interface range fa0/3-4    <br>
 switchport mode access    <br>
 switchport access vlan 10     <br>

interface range fa0/1   <br>
 switchport mode access    <br>
 switchport access vlan 10     <br>
exit      <br>

interface fastEthernet0/5-7   <br>
 switchport mode access       <br>
 switchport access vlan 20           <br>
exit     <br>

interface fastEthernet0/8-10      <br>
 switchport mode access       <br>
 switchport access vlan 30      <br>
exit           <br>
!    <br>

## TRUNK Configuration     <br>

!      <br>
Trunk Port        <br>
interface fastEthernet0/24     <br>
 switchport mode trunk      <br>
 switchport trunk allowed vlan 10,20,30         <br>
exit         <br>
!         <br>




<img width="973" height="323" alt="Image" src="https://github.com/user-attachments/assets/9adcb70b-3e9e-41a0-811b-88aecec0e84f" />

 ## DHCP Configuration
Router configured with DHCP pools for each VLAN.    <br>
Devices automatically receive IP addresses.   <br>

!      <br>
DHCP Configuration       <br>

ip dhcp pool vlan10     <br>
 network 192.168.1.0 255.255.255.0       <br>
 default-router 192.168.1.1     <br>
 dns-server 192.168.1.1       <br>

ip dhcp pool vlan20        <br>
 network 192.168.2.0 255.255.255.0     <br>
 default-router 192.168.2.1       <br>
 dns-server 192.168.2.1        <br>

ip dhcp pool vlan30           <br>
 network 192.168.3.0 255.255.255.0     <br>
 default-router 192.168.3.1        <br>
 dns-server 192.168.3.1       <br>
 !
 

<img width="576" height="214" alt="Image" src="https://github.com/user-attachments/assets/2eea47a8-4edf-4ea9-b0a6-1150910ebd55" />
<img width="799" height="355" alt="Image" src="https://github.com/user-attachments/assets/5d89125c-b0b0-456b-bec7-3fed35ae438e" />

 ## Inter-VLAN Routing    <br>
Router-on-a-Stick method implemented using sub-interfaces. <br>
Each sub-interface assigned to one VLAN.  <br>

!     <br>
interface GigabitEthernet0/0       <br>
 no ip address      <br>
 duplex auto         <br>
 speed auto      <br>

interface GigabitEthernet0/0.10     <br>
 encapsulation dot1Q 10        <br>
 ip address 192.168.1.1 255.255.255.192     <br>

interface GigabitEthernet0/0.20    <br>
 encapsulation dot1Q 20      <br>
 ip address 192.168.1.65 255.255.255.192      <br>

interface GigabitEthernet0/0.30      <br>
 encapsulation dot1Q 30        <br>
 ip address 192.168.1.129 255.255.255.192    <br>
!      <br>

<img width="981" height="363" alt="Image" src="https://github.com/user-attachments/assets/3994d820-714b-4f09-a734-c8ef20d2a00e" />

## SSH Configuration
SSH enabled on the router for secure remote management.    <br>
Local user accounts configured with username & password.    <br>

 !      <br>      
username mani password 0 mani@123     <br>
ip domain-name mani.com      <br>
crypto key generate rsa       <br>
ip ssh version 2        <br>
 
line vty 0 3       <br>
 login local        <br>
 transport input ssh       <br>

<img width="824" height="557" alt="Image" src="https://github.com/user-attachments/assets/3460774a-4a82-4153-ba20-d0f7ab5ec140" />
<img width="951" height="127" alt="Image" src="https://github.com/user-attachments/assets/a4373593-0342-43de-869d-626ed7f616b4" />








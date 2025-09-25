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

<img width="973" height="323" alt="Image" src="https://github.com/user-attachments/assets/9adcb70b-3e9e-41a0-811b-88aecec0e84f" />

 ## DHCP Configuration
Router configured with DHCP pools for each VLAN.    <br>
Devices automatically receive IP addresses.   <br>

<img width="576" height="214" alt="Image" src="https://github.com/user-attachments/assets/2eea47a8-4edf-4ea9-b0a6-1150910ebd55" />
<img width="799" height="355" alt="Image" src="https://github.com/user-attachments/assets/5d89125c-b0b0-456b-bec7-3fed35ae438e" />

 ## Inter-VLAN Routing
Router-on-a-Stick method implemented using sub-interfaces. <br>
Each sub-interface assigned to one VLAN.  <br>

  
## SSH Configuration
SSH enabled on the router for secure remote management.    <br>
Local user accounts configured with username & password.    <br>

<img width="824" height="557" alt="Image" src="https://github.com/user-attachments/assets/3460774a-4a82-4153-ba20-d0f7ab5ec140" />
<img width="951" height="127" alt="Image" src="https://github.com/user-attachments/assets/a4373593-0342-43de-869d-626ed7f616b4" />






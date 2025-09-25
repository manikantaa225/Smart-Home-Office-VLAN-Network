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


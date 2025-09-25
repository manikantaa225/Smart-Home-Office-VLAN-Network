# Smart-Home-Office-VLAN-Network
This project demonstrates the design and implementation of a Smart Home-Office Network using Cisco Packet Tracer. The network integrates VLANs, DHCP, SSH, and Inter-VLAN Routing (Router-on-a-Stick method) to ensure efficient communication and secure management.
## Project Overview
The objective of this project is to design a small-scale home-office hybrid network that:
Divides users into separate VLANs for logical segmentation.
Provides dynamic IP addressing using DHCP.
Allows secure remote access using SSH.
Enables communication between VLANs using Router-on-a-Stick.
Connects both wired and wireless devices (Laptops, PCs, Smartphones, Printers).

 ## Network Topology

The topology includes:
Router (1) – Configured with sub-interfaces for Inter-VLAN Routing.
Switch (1) – Central device for VLAN segmentation.
Access Points (3) – Wireless connectivity for smartphones & laptops.
End Devices – Laptops, PCs, Printers, Smartphones across VLANs.
Each VLAN represents a different department/zone:
VLAN 10 (Blue Zone) – Laptop0, Smartphone0, PC0, Printer0
VLAN 20 (Purple Zone) – Laptop1, Smartphone1, PC1, Printer1
VLAN 30 (Pink Zone) – Laptop2, Smartphone2, PC2, Printer2


# Date : 22.10.26
## Ex.-No-2-Interconnecting-Two-LANs-Using-a-Router-Basic-Router-Configuration


# Objective
To configure a router to connect two separate LANs and enable communication between them using static IP addressing.
________________________________________
# Apparatus/Tools Required
•	Cisco Packet Tracer<br>
•	2 PCs<br>
•	2 Switches<br>
•	1 Router (e.g., 1841 or 2911)<br>
•	Straight-through cables<br>
________________________________________
# Network Topology Diagram
 Description:<br>
•	PC0 → Switch0 → Router (FastEthernet0/0)<br>
•	PC1 → Switch1 → Router (FastEthernet0/1)<br>



<img width="1917" height="1198" alt="Screenshot 2026-10-22 161539" src="https://github.com/user-attachments/assets/a870fabb-a979-4c66-8ea4-7337974ed8cc" />

________________________________________
# IP Addressing Table
Device	Interface	IP Address	Subnet Mask<br>
PC0	NIC	192.168.1.10	255.255.255.0<br>
PC1	NIC	192.168.2.10	255.255.255.0<br>
Router0	FastEthernet0/0	192.168.1.1	255.255.255.0<br>
Router0	FastEthernet0/1	192.168.2.1	255.255.255.0<br>
________________________________________
# Procedure
1.	Open Cisco Packet Tracer and add 2 PCs, 2 Switches, and 1 Router.
2.	Connect each PC to a switch, and each switch to the router using straight-through cables.
3.	Assign IP addresses to both PCs according to the IP table.
4.	Configure the router interfaces:
o	FastEthernet0/0 → 192.168.1.1
o	FastEthernet0/1 → 192.168.2.1
5.	Use no shutdown on both router interfaces to activate them.
6.	Set each PC’s default gateway:<br>
o	PC0 → 192.168.1.1<br>
o	PC1 → 192.168.2.1<br>
7.	Test connectivity using ping from PC0 to PC1.<br>
________________________________________
# Commands Used (Router CLI)
bash<br>
CopyEdit<br>
Router> enable<br>
Router# configure terminal<br>
Router(config)# interface fastethernet0/0<br>
Router(config-if)# ip address 192.168.1.1 255.255.255.0<br>
Router(config-if)# no shutdown<br>

Router(config)# interface fastethernet0/1<br>
Router(config-if)# ip address 192.168.2.1 255.255.255.0<br>
Router(config-if)# no shutdown<br>
________________________________________
# Output (Screenshots)
•	Router CLI configuration<br>
•	IP configurations on PCs<br>
•	Successful ping between PC0 and PC1<br>

<img width="1918" height="1198" alt="Screenshot 2026-10-22 161635" src="https://github.com/user-attachments/assets/794e47e2-c24c-4b41-a880-29531406f7be" />


<img width="1918" height="1197" alt="Screenshot 2026-10-22 161822" src="https://github.com/user-attachments/assets/235eb67c-4b72-4c16-9ef8-25cb9718f1d9" />

<img width="1918" height="1195" alt="Screenshot 2026-10-22 161840" src="https://github.com/user-attachments/assets/ccc161b8-b6ec-4e8c-b8d0-c2345de23330" />



<img width="1918" height="1198" alt="Screenshot 2026-10-22 161909" src="https://github.com/user-attachments/assets/f35683d2-1840-4a67-b611-a4a04daf6f8f" />


<img width="1915" height="1193" alt="Screenshot 2026-10-22 161926" src="https://github.com/user-attachments/assets/255f5993-29b8-4665-b890-88c8ab3b8dd7" />


<img width="1918" height="1198" alt="Screenshot 2026-10-22 162154" src="https://github.com/user-attachments/assets/48eb017b-bfd1-41e0-bdfb-280caa785806" />


______________________________________





# Result





Successfully configured a router to connect two LANs. Communication between PC0 and PC1 across different networks was tested and verified.


<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups(NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Create 2 virtual machines.
- Install wireshark and observe ping communication between both virtual machines.
- Add Network Security rule to Linux and observe changes.

<h2>Actions and Observations</h2>

<p>
  
![2 VMs](https://github.com/user-attachments/assets/0b6e57f0-45ac-482b-b88f-2039b9ce730f)

</p>
<p>
First, we create 2 virtual machines. A windows and a Linux. This will be to observe the traffic between the 2.
</p>
<br />

<p>
  
![Wireshark and traffic](https://github.com/user-attachments/assets/c85fd512-d5ca-4f94-9885-c53b629c6d2a)

</p>
<p>
Next we install wireshark into our windows virtual machine. This software will allow us to inspect incoming and outgoing traffic. After it's been installed we run a ping test to the Linux virtual machine from the windows virtual machine using powershell. Within wireshark we can see the packets being sent and being received. It also provides further information such as MAC address of source and destination. 
</p>
<br />

<p>
  
![Security and Time out](https://github.com/user-attachments/assets/1a3b45af-e4e3-4080-bb28-572476f9c682)

</p>
<p>
Lastly, we run a network security rule for our Linux virtual machine. This will act like a firewall for incoming traffic. We can see that once the "rule" was added to "deny" ICMPv4 traffic, our windows virtual machine times out every time it makes a ping request to the Linux virtual machine. 
</p>
<br />

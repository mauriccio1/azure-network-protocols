<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Step 1
- Step 2
- Step 3
- Step 4

<h2>Actions and Observations</h2>

<p>
<img src="https://i.imgur.com/TVHa8fs.png" height="80%" width="80%" alt="create linux VM"/>
</p>
<p>
In the Azure portal create a resource a group and two VM (one running Windows 10 and one running Linux-based Ubuntu).
</p>
<br />

<p>
<img src="https://i.imgur.com/EOel9JP.png" height="80%" width="80%" alt="download wireshark"/>
</p>
<p>
login into the Windows VM and download the application Wireshark.
</p>
<br />

<p>
<img src="https://i.imgur.com/A1uzkTq.png" height="80%" width="80%" alt="new inbound rule"/>
</p>
From The Windows 10 VM, open the command line or PowerShell and attempt to ping a public website (such as www.google.com) and observe the traffic in Wireshark
Initiate a perpetual/non-stop ping from your Windows 10 VM to your Ubuntu VM.
enable ICMP traffic for the Network Security Group your Ubuntu VM is using
Back in the Windows 10 VM, observe the ICMP traffic in WireShark and the command line Ping activity.
  
</p>
<br />

<p>
<img src="https://i.imgur.com/ByqOCgA.png" height="80%" width="80%" alt="install wireshark/observe SSH"/> 
</p>
<p>
Back in Wireshark, filter for SSH traffic only
From your Windows 10 VM, “SSH into” your Ubuntu Virtual Machine (via its private IP address). <br/>
Type commands (username, pwd, etc) into the linux SSH connection and observe SSH traffic spam in WireShark. <br/>
Exit the SSH connection by typing ‘exit’ and pressing [Enter]

</p>
<br />

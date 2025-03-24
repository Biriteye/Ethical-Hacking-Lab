# ARP cache poisoning and MITM attacks

## Objective

This lab project focuses on network security and penetration testing, specifically demonstrating an ARP poisoning attack to perform a Man-in-the-Middle (MITM) attack within a local virtual network. I will import a pre-configured virtual lab environment, including Kali Linux, a Debian client, and a Windows server, into VirtualBox. I will utilize nmap to discover hosts and configure Ettercap to perform ARP poisoning.

### Skills Learned

- Network scanning and host discovery using nmap.
- ARP protocol analysis and manipulation.
- MITM attack execution using Ettercap.
- Network traffic analysis and packet sniffing.
- Using Ettercap filters for packet manipulation.
- Network security concepts and countermeasures.

### Tools Used

- Ettercap
- nmap
- Kali Linux
- Windows IIS Manager
- virtualBox


## IP Addresses:
- Kali: 192.168.0.100
- Windows Server: 192.168.0.100
- Debian Client: 192.168.0.101
  
## Steps
- Scan the network using nmap to ensure all 3 VMs are communicating
  <img src="https://i.postimg.cc/hjpHcV3V/Picture1.png" />

- Open the Ettercap GUI change listening to the internal network interface that has connectivity to the other VMs
  <img src="https://i.postimg.cc/RVCRMXGK/Picture2.png" />

- Perform a Host scan on Ettercap
  <br>
  <img src="https://i.postimg.cc/MZm52h0z/Picture3.png" />

- Check the ARP table from Windows and Debian before we use Ettercap to poison the tables
  <img src="https://i.postimg.cc/fLBV5jXQ/Picture4.png" />
  
  <img src="https://i.postimg.cc/Y9p41yvx/Picture5.png" />

- Back in Ettercap set the Windows and Debian as targets and initiate the poisoning attack
  <img src="https://i.postimg.cc/jjYvrK1d/Picture6.png" />
  
  <img src="https://i.postimg.cc/KzZNRfF6/Picture7.png" />
  
- Check the ARP tables to confirm that the Windows and Debian now have the same Mac address as the Kali machine
  <img src="https://i.postimg.cc/bwtLMd3B/Picture8.png" />

  <img src="https://i.postimg.cc/SKLdS30L/Picture9.png" />

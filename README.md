# ARP cache poisoning and MITM attacks

## Objective

This lab project focuses on network security and penetration testing, specifically demonstrating an ARP poisoning attack to perform a Man-in-the-Middle (MITM) attack within a local virtual network. I will import a pre-configured virtual lab environment, including Kali Linux, a Debian client, and a Windows server, into VirtualBox. I will utilize nmap to discover hosts, explore web services on the Debian client, and configure Ettercap to perform ARP poisoning.

### Skills Learned

- Network scanning and host discovery using nmap.
- ARP protocol analysis and manipulation.
- MITM attack execution using Ettercap.
- Network traffic analysis and packet sniffing.
- Web application vulnerability assessment.
- Using Ettercap filters for packet manipulation.
- Basic web request analysis using wget.
- Network security concepts and countermeasures.

### Tools Used

- Ettercap
- nmap
- wget
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

- Open the Ettercap GUI and ensure it is listening on the internal network interface that has connectivity to the other VMs
  <img src="https://i.postimg.cc/RVCRMXGK/Picture2.png" />

# Identify-and-Remediate-Vulnerabilities

## Objective

Utilize Metasploitable2 and OpenVAS to identify and remediate vulnerabilities in a simulated network environment. This involves scanning for vulnerabilities, analyzing the results, and applying appropriate remediation techniques to secure the system. The goal is to enhance skills in vulnerability assessment, exploit identification, and system hardening.

### Skills Learned

- Virtualization: Setting up virtual machines using VM Workstation.
- Network Configuration: Setting up network interfaces and assigning IP addresses.
- Vulnerability Assessment: Analyzing scan results to identify vulnerabilities and their severity.
- Documentation: Documenting the steps taken and results obtained during the project.
- System Configuration: Configuring OpenVAS using setup commands.

### Tools Used

- Metasploitable2: A purposely vulnerable virtual machine used for practicing exploitation techniques.
- OpenVAS: Open-source vulnerability scanner and manager for assessing and managing network security.
- nano: A text editor used for editing system configuration files.
- Ping: Network utility used to test the reachability of a host on an IP network.

## Steps

*Ref 1*
![kali-linux-2024 1-vmware-amd64-2024-05-28-22-41-40](https://github.com/Casttllee/Identify-and-Remediate-Vulnerabilities/assets/137667912/a602ca14-c4f3-4792-ba10-4cad95092c33)
 I started this project by downloading and installing Metasploitable2 and kali linux for VM workstation. The next step was to make sure the repositories and up to date. I did this by using the "sudo apt-get update && sudo apt-get upgrade -y".

*Ref 2*
![kali-linux-2024 1-vmware-amd64-2024-05-28-23-08-46](https://github.com/Casttllee/Identify-and-Remediate-Vulnerabilities/assets/137667912/fed8a46d-8bb7-4430-8122-998661fa7685)
 Next, I began to install OpenVAS by typing "sudo apt install gvm".

*Ref 3*
![kali-linux-2024 1-vmware-amd64-2024-05-28-23-09-44](https://github.com/Casttllee/Identify-and-Remediate-Vulnerabilities/assets/137667912/461b6c45-2b85-4dd0-9a6c-4208c8aef0d6)
 Afterward, I typed "sudo gvm-setup", which started the setup and installation process.

*Ref 4*
![kali-linux-2024 1-vmware-amd64-2024-05-29-20-42-25](https://github.com/Casttllee/Identify-and-Remediate-Vulnerabilities/assets/137667912/61e82b65-9667-47f5-91df-a08eefb32cf2)
 I then ran the command "gvm-check-setup" to make sure everything is configured correctly.The output stated that the installation is ok.

*Ref 5*
![kali-linux-2024 1-vmware-amd64-2024-05-29-21-00-26](https://github.com/Casttllee/Identify-and-Remediate-Vulnerabilities/assets/137667912/8a585243-9268-4b24-8bcb-269460dae587)
 Following that, I went on firefox and entered the address "https://localhost:9392" which prompted me to login into Greenbone. 

*Ref 6*
![Metasploitable2-Linux-2024-05-29-21-08-10](https://github.com/Casttllee/Identify-and-Remediate-Vulnerabilities/assets/137667912/4555aad1-141a-4d69-aa29-df7074953f12)
 After logging onto Greenbone, I started my Metasploitable2 machine.

*Ref 7*
![Metasploitable2-Linux-2024-05-29-21-14-08](https://github.com/Casttllee/Identify-and-Remediate-Vulnerabilities/assets/137667912/a01715c9-00c1-4482-ab85-4c031dd2f97b)
 Next, I used he command "ip a" to look at the network adapter, which was set to "eth0".

*Ref 8*
![Metasploitable2-Linux-2024-05-29-21-17-49](https://github.com/Casttllee/Identify-and-Remediate-Vulnerabilities/assets/137667912/3ac533e3-f372-41da-9298-c4cb7e95ebc6)
 The next step was to set an IP address for the network adapter. I completed this by typing the command "sudo nano /etc/network/interfaces".

*Ref 9*
![Metasploitable2-Linux-2024-05-29-21-20-14](https://github.com/Casttllee/Identify-and-Remediate-Vulnerabilities/assets/137667912/eff46eb2-bd81-4a8e-99b6-1850ad11d5db)
 The last step I completed on Metasploitable2 was setting the network adapter from DHCP to static because I am manually assigning an address. I then typed the IP address and netmask and saved. *Ref 9* shows the IP is set correctly.
 
*Ref 10*
![kali-linux-2024 1-vmware-amd64-2024-05-29-21-30-09](https://github.com/Casttllee/Identify-and-Remediate-Vulnerabilities/assets/137667912/d107d64e-483c-435f-ab59-22b3d8a1b835)
 Going back on Linux, I viewed the network interfaces which showed eth1 having no IP address.

*Ref 11*
![kali-linux-2024 1-vmware-amd64-2024-05-29-21-31-53](https://github.com/Casttllee/Identify-and-Remediate-Vulnerabilities/assets/137667912/10c619d1-c83f-450b-8884-396b627bc195)
 I then manually assigned an IP address by going to settings to Advanced Network Configuration. Wired connection 2 showed it was the correct network adapter.

*Ref 12*
![kali-linux-2024 1-vmware-amd64-2024-05-29-21-51-03](https://github.com/Casttllee/Identify-and-Remediate-Vulnerabilities/assets/137667912/0b100848-5662-4fec-9982-782da102832a)
 Following that, I navigated to the IPv4 settings. In the settings I changed the method to manual as well as added an IP address and Netmask.

*Ref 13*
![kali-linux-2024 1-vmware-amd64-2024-05-29-21-51-39](https://github.com/Casttllee/Identify-and-Remediate-Vulnerabilities/assets/137667912/84e4e175-b2b0-4680-a816-b26b6a592e6a)
 As a result, eth1 was assigned an IP address.

*Ref 14*
![kali-linux-2024 1-vmware-amd64-2024-05-29-21-53-46](https://github.com/Casttllee/Identify-and-Remediate-Vulnerabilities/assets/137667912/78da7578-b653-433f-8468-b26b56ee078f)
 Moving forward, I used the command "ping" to ping the IP address on my Metasploitable machine. The response provided proof connectivity.

 *Ref 15*
![kali-linux-2024 1-vmware-amd64-2024-05-29-22-01-24](https://github.com/Casttllee/Identify-and-Remediate-Vulnerabilities/assets/137667912/6ee98662-9925-426f-a302-ea548a06e8b7)
 In the next phase I created a target to be scanned.

 *Ref 16*
![Screenshot (27)](https://github.com/Casttllee/Identify-and-Remediate-Vulnerabilities/assets/137667912/e374eb84-1ac8-4c4f-8ffe-251cab4061a2)
 I then created a new task for a scan by selecting my target as well as an OpenVAS Default scanner and a Full and fast Scan Cofig.

 *Ref 17*
![Screenshot (28)](https://github.com/Casttllee/Identify-and-Remediate-Vulnerabilities/assets/137667912/fd7e82c1-7a2a-4ed8-8a4d-1cf99cc97a8a)
 Lastly, I can view the given results of the scan, showing vulnerabilities and their severity.
 
## Conclusion 
In conclusion, this project demonstrated a comprehensive exploration of setting up and configuring a secure testing environment for vulnerability assessment and penetration testing purposes. Through the installation and configuration of Metasploitable2, Kali Linux, and OpenVAS within virtualized environments, fundamental skills in system administration, network configuration, and security assessment were honed. The systematic approach to updating repositories, installing software packages, and configuring network interfaces underscored the importance of meticulous attention to detail in ensuring the stability and security of the environment.

By leveraging tools such as apt-get for package management, OpenVAS for vulnerability scanning, and Firefox for web interface access, this project showcased the practical application of various software tools in the cybersecurity domain. Moreover, the manual assignment of IP addresses and network troubleshooting highlighted the necessity of understanding underlying network principles for effective system configuration and management.

Ultimately, this project not only provided hands-on experience in setting up a secure testing environment but also underscored the importance of continuous learning and adaptation in the ever-evolving field of cybersecurity. Through documentation and reflection on the steps taken and challenges encountered, valuable insights were gained, laying a solid foundation for future endeavors in cybersecurity and beyond.

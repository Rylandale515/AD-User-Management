<h1>Active Directory User Management</h1>

<h2>Description</h2>
This project focuses on the implementation of Active Directory User Management using Windows Server 2019 and Windows 10 VMs in an Oracle VirtualBox environment. The goal is to create a functional Active Directory domain, set up users, and manage network services such as DHCP, DNS, NAT, and Remote Access.
<br />
<br />

<h2>Languages and Utilities Used</h2>

- <b>Programming Languages:</b>
  - PowerShell

- <b>Virtualization Platform:</b>
  - Oracle VirtualBox

- <b>Operating Systems:</b>
  - Windows Server 2019
  - Windows 10
<br />
<br />

<h2>Environments Used </h2>

- <b>Hypervisor:</b>
  - Oracle VirtualBox

- <b>Virtual Machines:</b>
  - Windows Server 2019 (Domain Controller - DC)
  - Windows 10 (Client - CLIENT1)
<br />
<br />

<h2>Program walk-through:</h2>

1. <b>Setting Up Virtual Environment:</b>
  - Installed Oracle VirtualBox and the corresponding extension pack.
  - Created VMs for the Domain Controller (DC) and Client (CLIENT1).
  - Configured VM settings, including RAM, storage, and CPUs.
<br />

2. <b>Installing Windows Server 2019:</b>
  - Installed Windows Server 2019 on the DC VM.
  - Configured network adapters for internal and internet connections.
  - Installed VirtualBox Guest Additions for improved functionality.
<br />

3. <b>Configuring Domain Controller:</b>
  - Renamed the DC machine to "DC" and set up a domain: rylanstalnaker.com.
  - Added an administrator account and created an admin group (_ADMINS).
  - Configured Routing and Remote Access (RAS and NAT) for internet connectivity.
<br />
<p align="center">
  Labeling Network Adapters:<br/>
  <img width="50%" height="50%" src="https://i.imgur.com/5cLXRp6.png">
  <br/>
  <br/>
  Configuring IP Addresses:<br/>
  <img width="50%" height="50%" src="https://i.imgur.com/97S77ej.png">
</p>
<br />

4. <b>Setting Up DHCP Server:</b>
  - Installed DHCP Server role on the DC.
  - Configured a DHCP scope (172.16.0.100-200) with necessary options.
<br />

5. <b>Adding Users with PowerShell Script:</b>
  - Created a PowerShell script to add 1,000 users to the AD.
  - Generated usernames based on the first initial and last name.
  - Set up user properties, including passwords and group memberships.
<br />
<p align="center">
  Users Created from Script:<br/>
  <img width="80%" height="80%" src="https://i.imgur.com/Swh12Od.png">
</p>
<br/>

6. <b>Setting Up Windows 10 Client:</b>
  - Installed Windows 10 on the CLIENT1 VM.
  - Checked DHCP functionality by verifying the assigned IP address.
<br />

7. <b>Resolving DNS Issues:</b>
  - DNS was routed to internal IP address, had to change to IP address facing the internet.
  - Corrected DNS routing on the DC to resolve internet connectivity issues on the client.
<br />
<p align="center">
  Pinging Google using DNS:<br/>
  <img width="100%" height="100%" src="https://i.imgur.com/VWU9W2n.png">
</p>
<br/>

8. <b>Joining Client to Domain:</b>
  - Changed the client name to CLIENT1 and joined it to the rylanstalnaker.com domain.
  - Logged in using AD user credentials, confirming successful domain integration.
<br />
<p align="center">
  Renaming Client1 & Joining Domain:<br/>
  <img width="100%" height="100%" src="https://i.imgur.com/M1vVFVp.png">
</p>
<br/>

9. <b>Verification:</b>
  - Checked user authentication using the "whoami" command on the client.
<br />
<p align="center">
  Verifying Login to Domain AD Account:<br/>
  <img width="80%" height="80%" src="https://i.imgur.com/mbee5Td.png">
</p>
<br />
<br/>

<h3>Conclusion</h3>
This project showcases the successful implementation of an Active Directory User Management system using Windows Server, VirtualBox, and PowerShell. It demonstrates proficiency in configuring network services, managing users, and integrating client machines into the domain. The provided documentation serves as a comprehensive guide for setting up a similar environment.

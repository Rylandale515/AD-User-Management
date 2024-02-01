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

4. <b>Setting Up DHCP Server:</b>
  - Installed DHCP Server role on the DC.
  - Configured a DHCP scope (172.16.0.100-200) with necessary options.
<br />

5. <b>Adding Users with PowerShell Script:</b>
  - Created a PowerShell script to add 1,000 users to the AD.
  - Generated usernames based on the first initial and last name.
  - Set up user properties, including passwords and group memberships.
<br />

6. <b>Setting Up Windows 10 Client:</b>
  - Installed Windows 10 on the CLIENT1 VM.
  - Checked DHCP functionality by verifying the assigned IP address.
<br />

7. <b>Resolving DNS Issues:</b>
  - DNS was routed to internal IP address, had to change to IP address facing the internet.
  - Corrected DNS routing on the DC to resolve internet connectivity issues on the client.
<br />

8. <b>Joining Client to Domain:</b>
  - Changed the client name to CLIENT1 and joined it to the rylanstalnaker.com domain.
  - Logged in using AD user credentials, confirming successful domain integration.
<br />

9. <b>Verification:</b>
  - Checked user authentication using the "whoami" command on the client.
<br />
<br />

<h3>Conclusion</h3>
This project showcases the successful implementation of an Active Directory User Management system using Windows Server, VirtualBox, and PowerShell. It demonstrates proficiency in configuring network services, managing users, and integrating client machines into the domain. The provided documentation serves as a comprehensive guide for setting up a similar environment.

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>

<!--
![CreateADDNS5](https://github.com/Rylandale515/AD-User-Management/assets/34111857/28c8fb26-8389-4fa5-8b56-515333f4b255)
![DNSCreation6](https://github.com/Rylandale515/AD-User-Management/assets/34111857/305c9812-5525-40cd-a793-a71b02ae31b0)
![GuestAdditionsCD](https://github.com/Rylandale515/AD-User-Management/assets/34111857/3e3565d4-b8a4-497b-823d-4eb2fb9236f4)
![GuestAdditionsCD2](https://github.com/Rylandale515/AD-User-Management/assets/34111857/71492e96-4d7d-4fc8-abb0-15a8e5184e10)
![LoginDomain](https://github.com/Rylandale515/AD-User-Management/assets/34111857/a50f2655-85c9-499e-b56f-b7b23b89a893)
![NetworkAdapters3](https://github.com/Rylandale515/AD-User-Management/assets/34111857/d1a765ff-85d4-4a50-9c67-147cf3d4a28e)
![PingDNS](https://github.com/Rylandale515/AD-User-Management/assets/34111857/e45475e6-6d8a-4dc4-b042-945fd325b74e)
![RAS7](https://github.com/Rylandale515/AD-User-Management/assets/34111857/f9ed5cb2-be5b-46c6-ad75-dd7dc6584b7d)
![RenameClient](https://github.com/Rylandale515/AD-User-Management/assets/34111857/5194d19c-4b4e-4141-b55a-b7eb3cabd602)
![RenameClient2](https://github.com/Rylandale515/AD-User-Management/assets/34111857/3d5da51a-1e2e-45d1-98bd-4c19b6b7df03)
![SetInternalIP4](https://github.com/Rylandale515/AD-User-Management/assets/34111857/898c7276-b00a-4896-936f-e02409533526)
![UserLoggedIntoDomain](https://github.com/Rylandale515/AD-User-Management/assets/34111857/dd9c909c-5282-4c74-a2ab-e454a6b29937)
![Users8](https://github.com/Rylandale515/AD-User-Management/assets/34111857/5182297d-ea38-4ba4-93cb-9fa0daad2629)
![VMSettings1](https://github.com/Rylandale515/AD-User-Management/assets/34111857/d77a3931-8130-4113-952d-038f5a4e625b)


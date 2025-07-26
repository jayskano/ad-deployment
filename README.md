<p align="center">
  <img src="https://github.com/user-attachments/assets/a60432c2-d616-46bc-a9de-e813a2a88036" width="600" />
</p>

<h1>Preparing Active Directory Infrastructure in the Cloud (Azure)</h1>
This project demonstrates how I create the Active Directory infrastructure within Azure. This will be used to deploy and configure Active Directory in a future project.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (22H2)


<h2>Walkthrough</h2>

<p>
<img src="https://github.com/user-attachments/assets/54b7af3c-5924-4911-9a0d-69ef812fe9cd" width=800/>
</p>
<p>

  - To begin the project, I created a new Resource Group and two Virtual Machines in Azure. Both VMs were set to to the same Virtual Network and Region.
  - I named the first VM "DC-1" (Domain Controller), set the image to Windows Server 2022, and selected a size with 2vcpus and 8 Gib memory.
  - I named the second VM "Client-1", set the image to "Windows 10, and selected a size with 2 vcpus and 8 Gib memory.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/5cfc4883-ea5b-4992-8aef-4691a16e3078" width=800/>
</p>
<p>

  - After creating the VMs, I naviagted to the network settings of the DC-1 Virtual Machine and located the Network Interface.

</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/971f1c68-6b59-40c9-9aa3-cd9f6edff8f4" width=800/>
</p>
<p>

  - Within IP Configuration, I selected "ipconfig" and changed the Allocation to "Static" under Private IP address settings.
  - This will ensure that the Private IP address for DC-1 doesn't change.

</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/09a5a585-ef47-479b-b32d-ac6c94bb9bc2" width=400/>
</p>
<p>

  - Next, I went into Remote Desktop Connection and connected to DC-1 using the Public IP address.

</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/fde96e3f-549f-4633-a722-3361d4c98cd5" width=400 />
</p>
<p>

  - After successfully connecting to DC-1, I selected run from the start menu and entered "wf.msc".
  - This will open the firewall settings for DC-1.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/943af104-f814-438e-adaa-0a2cf102fdb0" width=800/>
</p>
<p>

  - Within the firewall settings, I selected Windows Defender Firewall Properties.
  - I changed the firewall state for Domain, Private Profile, and Public Profile to Off.

</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/bb91dd38-cf4f-4208-9f66-e4c3c8fa2c71" width=800 />
</p>
<p>

  - Next, I went back into azure and selected Client-1.
  - Under the Network Settings, I selected "Network Interface / IP Configuration"



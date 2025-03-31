
![Screenshot 2025-03-15 190857](https://github.com/user-attachments/assets/5ac6045a-86bf-4b1a-b068-d695f4e7820e)


</p>

<h1>Preparing AD Infrastructure in (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Step 1
- Step 2
- Step 3
- Step 4

<h2>Deployment and Configuration Steps</h2>

<p>
  
![Screenshot 2025-03-09 200145](https://github.com/user-attachments/assets/40ee0a8a-c425-4d2d-bb59-ef56b78c9113)


</p>
<p>
Open Microsoft Azure create a new resource group.
</p>
<br />

<p>
  
![Screenshot 2025-03-09 200509](https://github.com/user-attachments/assets/81ad8671-396b-46a4-8637-72c953128b09)

</p>
<p>
Name the resource group and select the region.
</p>
<br />

<p>
  
![Screenshot 2025-03-09 200529](https://github.com/user-attachments/assets/9d42c839-88c3-43a4-9dcb-5bf0d31dd498)

</p>
<p>
Review and create the resource group.
</p>
<br />

<p>
  
![Screenshot 2025-03-09 200539](https://github.com/user-attachments/assets/0beb4f54-fe41-4635-822a-17351518185b)

</p>
<p>
The resource group has been created succesfully.
</p>
<br />

<p>
  
![Screenshot 2025-03-09 200602](https://github.com/user-attachments/assets/0046ffdd-b8a5-4795-9c69-14f96c19bd76)


</p>
<p>
Next, search for "Virtual networks"to manually create the virtual network for the domain controller.
</p>
<br />

<p>
  
![Screenshot 2025-03-09 200657](https://github.com/user-attachments/assets/bdac57c4-b026-4422-8e91-480209437c47)

</p>
<p>
While creating the virtual network, select the Active-Directory-Lab resource group and name the virtual network.
</p>
<br />

<p>
  
![Screenshot 2025-03-09 200823](https://github.com/user-attachments/assets/2b31f7e4-bafd-4432-a954-2875f69de2fb)


</p>
<p>
Create the first virtual machine for the domain controller.
<br />

<p>
  
![Screenshot 2025-03-09 201029](https://github.com/user-attachments/assets/dfbab031-c9d6-47ca-aad6-db8ca9ed6444)

</p>
<p>
Rename the vm to dc-1 and make cure the reigon is the same as the Active-Directory-Lab resource group.
</p>
<br />

<p>
  
![Screenshot 2025-03-09 201039](https://github.com/user-attachments/assets/0041922f-1989-4093-8b6c-b3b6e619b5d7)


</p>
<p>
Select the Windows Server 2022
</p>
<br />

<p>
  
![Screenshot 2025-03-09 201225](https://github.com/user-attachments/assets/37991685-d579-4726-9520-aded0e6c231c)


</p>
<p>
Make sure the resource group is Active-Directory-Lab.
</p>
<br />

<p>
  
![Screenshot 2025-03-09 201707](https://github.com/user-attachments/assets/50ce7ce9-6366-40e3-9571-88eb6746a3e0)

</p>
<p>
Deployed the Active-DirectoryVnet.
</p>
<br />

<p>
  
![Screenshot 2025-03-09 201724](https://github.com/user-attachments/assets/acad2348-5d6d-4f48-aa60-789ef578e351)

</p>
<p>
The Active-DirectoryVnet was deployed successfully.
</p>
<br />

<p>
  
![Screenshot 2025-03-09 203418](https://github.com/user-attachments/assets/a1e30227-0b90-4f81-9589-8da661c2d3a9)


</p>
<p>
In the Networking Tab select the Active-DirectoryVnet. Other settinfgs should be left as is.
</p>
<br />

<p>
  
![Screenshot 2025-03-09 203443](https://github.com/user-attachments/assets/f3257ae6-e0ba-449a-9d1a-2dfa42c742aa)

</p>
<p>
Review and create the domain controller vm.
</p>
<br />

<p>
  
![Screenshot 2025-03-09 203453](https://github.com/user-attachments/assets/a1e39b10-02eb-4044-a691-83ebab1efc5a)

</p>
<p>
The domain controller submitted for deployment.
</p>
<br />

<p>
  
![Screenshot 2025-03-09 203458](https://github.com/user-attachments/assets/e77b12e4-9e38-48cd-8ac1-d5e8fab1af2c)


</p>
<p>
Deployment in progress.
</p>
<br />

<p>
  
![Screenshot 2025-03-09 203515](https://github.com/user-attachments/assets/0d272c25-fb6c-434a-a5f3-e5cfaa35f479)


</p>
<p>
Next, create another virtual machine for the client.
</p>
<br />

<p>
  
![Screenshot 2025-03-09 203540](https://github.com/user-attachments/assets/9f4a220e-bb4d-4e93-9eb3-c045897d9e8a)


</p>
<p>
Set the Active-Directory-Lab as the resource group, name the virtual machineand set the region. All other settings are left as is.
</p>
<br />

<p>
  
![Screenshot 2025-03-09 203602](https://github.com/user-attachments/assets/5d437087-e73f-48fc-8caa-34b12b24262b)

</p>
<p>
Set the size to at least 2 cores with 8GB of memory.
</p>
<br />

<p>
  
![Screenshot 2025-03-09 203631](https://github.com/user-attachments/assets/f84c41c8-bc62-41d6-9f65-41ffa6fcdd5c)


</p>
<p>
The image should be Windows 10 Pro version 22H2 x64 Gen2. In the Administrator account sectionset the username and password. After all the settings are set, review and create.
</p>
<br />

<p>
  
![Screenshot 2025-03-09 203738](https://github.com/user-attachments/assets/86608b99-5d3f-4e0c-a6a7-a37330170ae5)

</p>
<p>
Deployment for the client vm is in progress.
</p>
<br />

<p>
  
![Screenshot 2025-03-09 204211](https://github.com/user-attachments/assets/0046c6b0-e711-4d15-9c2c-8e3bf08fea07)

</p>
<p>
Navigate to the dc-1 virtual machine.
</p>
<br />

<p>
  
![Screenshot 2025-03-09 204235](https://github.com/user-attachments/assets/f038e59b-676a-49ad-b7f3-19702baee4d8)


</p>
<p>
Locate Network settings.
</p>
<br />

<p>
  
![Screenshot 2025-03-09 204308](https://github.com/user-attachments/assets/ab259763-b078-4cff-9f95-684c72cf0df9)

</p>
<p>
Click on the Network inteface/ IP configuration.
</p>
<br />

<p>
  
![Screenshot 2025-03-09 204321](https://github.com/user-attachments/assets/87583d1e-5bb1-4505-8731-44da9181df56)


</p>
<p>
Under settings, go to IP configurations, and click on ipconfig1
</p>
<br />

<p>
  
![Screenshot 2025-03-09 204353](https://github.com/user-attachments/assets/6cf22080-9482-4bb0-993a-954287968194)

</p>
<p>
Change the Allocation from Dynamic to Static and save the changes.
</p>
<br />

<p>
  
![Screenshot 2025-03-09 204403](https://github.com/user-attachments/assets/79bb3745-dbab-4109-9036-40ae0138b06e)

</p>
<p>
Notice that tha Private IP Address is set to Static.
</p>
<br />

<p>
  
![Screenshot 2025-03-09 204430](https://github.com/user-attachments/assets/ca576d76-d362-4bf3-ad21-ffa5791461d8)

</p>
<p>
Search for Virtual Machnies.
</p>
<br />

<p>
  
![Screenshot 2025-03-09 204438](https://github.com/user-attachments/assets/0b28811f-a1b8-43c8-87da-d91ce36d532e)

</p>
<p>
Select dc-1 vm.
</p>
<br />

<p>
  
![Screenshot 2025-03-09 204510](https://github.com/user-attachments/assets/bf1b4baa-0edc-44b0-b044-97b89fa3dd5a)

</p>
<p>
Locate the dc-1 Public IP address and copy it to Remote Desktop.
</p>
<br />

<p>
  
![Screenshot 2025-03-09 204533](https://github.com/user-attachments/assets/034e9c4d-e2d0-4a0d-9110-e37ebe847988)

</p>
<p>
Select Yes.
</p>
<br />

<p>
  
![Screenshot 2025-03-09 204629](https://github.com/user-attachments/assets/a0e6a552-b28b-4857-8a7e-a45595db87c9)

</p>
<p>
Upon logging into the domain controller successfully the server manager dashboard should open automatically.
</p>
<br />

<p>
  
![Screenshot 2025-03-09 204800](https://github.com/user-attachments/assets/7b059eda-0a5b-47d2-8d6e-58a799cc63be)

</p>
<p>
Right-click on the start icon and go to System.
</p>
<br />

<p>
  
![Screenshot 2025-03-09 204820](https://github.com/user-attachments/assets/fd39e363-a1bc-4191-be2e-fac649dfb825)

</p>
<p>
In the Windows specifications section, the Windows Server 2022 is the correct edition.
</p>
<br />

<p>
  
![Screenshot 2025-03-09 204854](https://github.com/user-attachments/assets/8894dba1-eaf7-4ef5-9fb6-cced65abd3ac)

</p>
<p>
Right-click on the start icon and select Run.
</p>
<br />

<p>
  
![Screenshot 2025-03-09 204907](https://github.com/user-attachments/assets/12024053-3a97-4654-8cfd-8f3de4fd5416)

</p>
<p>
In Run, type wf.msc to open up windows firewall.
</p>
<br />

<p>
  
![Screenshot 2025-03-09 205033](https://github.com/user-attachments/assets/734f5de1-6b7e-474a-9b84-2f29a41df596)

</p>
<p>
Click on properties and turn the Domain Profile firewall off.
</p>
<br />

<p>
  
![Screenshot 2025-03-09 205038](https://github.com/user-attachments/assets/dd57186c-b001-4a4a-a43b-42e62aa8c87c)

</p>
<p>
Turn the Private Profile firewall off.
</p>
<br />

<p>
  
![Screenshot 2025-03-09 205046](https://github.com/user-attachments/assets/def08e0a-1bec-469a-889b-e1eace138c56)

</p>
<p>
Turn the Public Profile firewall off.
</p>
<br />

<p>
  
![Screenshot 2025-03-09 205134](https://github.com/user-attachments/assets/53629b0e-7ec5-452b-9981-153ff3beabbc)

</p>
<p>
Observe that the firewall has been turned off.
</p>
<br />

<p>
  
![Screenshot 2025-03-09 205237](https://github.com/user-attachments/assets/4d619b1b-15ad-475b-acd8-f5ef5ab0a509)

</p>
<p>
Click on dc-1.
</p>
<br />

<p>
  
![Screenshot 2025-03-09 205321](https://github.com/user-attachments/assets/ef65a1d1-ea26-4bb4-aadd-41391fa2da7a)

</p>
<p>
Scroll to the Networking section and observe the private IP address.
</p>
<br />

<p>
  
![Screenshot 2025-03-09 205347](https://github.com/user-attachments/assets/a724aee9-1877-4d82-8b27-41d7fd03e707)

</p>
<p>
Go back to virtual machines and click on client-1.
</p>
<br />

<p>
  
![Screenshot 2025-03-09 205404](https://github.com/user-attachments/assets/8f3d98c3-8534-44f2-89c7-ceac8a516780)

</p>
<p>
Click on the Network interface/ IP configuration.
</p>
<br />

<p>
  
![Screenshot 2025-03-09 205433](https://github.com/user-attachments/assets/4f2bce66-7136-4024-a60a-c51dbb7ef0b5)

</p>
<p>
In the settings tab, go to DNS servers. It shows that the DNS servers is inherited fromthe virtual network.
</p>
<br />

<p>
  
![Screenshot 2025-03-09 205540](https://github.com/user-attachments/assets/bbbf1669-66aa-4508-b986-d6055cc2e078)

</p>
<p>
Click on custom and input dc-1 private ip address which is 10.0.0.4
</p>
<br />

<p>
  
![Screenshot 2025-03-09 205557](https://github.com/user-attachments/assets/70ce27d1-2dfe-4d05-9e94-9e11509dc11f)

</p>
<p>
Save the changes.
</p>
<br />

<p>
  
![Screenshot 2025-03-09 205627](https://github.com/user-attachments/assets/3ea57596-c089-47e2-9c95-ee92d557983c)

</p>
<p>
Go back to virtual machimes.
</p>
<br />

<p>
  
![Screenshot 2025-03-09 205647](https://github.com/user-attachments/assets/ba85f269-35df-4be5-b350-0c52d149cddf)

</p>
<p>
Select client-1, click on the three dots and restart the virtual machine.
</p>
<br />

<p>
  
![Screenshot 2025-03-09 205653](https://github.com/user-attachments/assets/65096ceb-5f14-44a8-aa67-c08692f313d7)

</p>
<p>
Click Yes.
</p>
<br />

<p>
  
![Screenshot 2025-03-09 205838](https://github.com/user-attachments/assets/6e82f287-577b-4c94-9ae2-c67b44cea804)

</p>
<p>
Open Remote Desktop and copy client-1 public IP address.
</p>
<br />

<p>
  
![Screenshot 2025-03-09 205902](https://github.com/user-attachments/assets/a0ca0995-fd7c-41fd-bc00-9a17d9def1d4)

</p>
<p>
Click Yes.
</p>
<br />

<p>
  
![Screenshot 2025-03-09 210309](https://github.com/user-attachments/assets/87171de5-4615-4576-830e-14abfc45e8a6)

</p>
<p>
Within the client-1 vm, search windows powershell, right-click and run as administrator.
</p>
<br />

<p>
  
![Screenshot 2025-03-09 210358](https://github.com/user-attachments/assets/25e6e40b-f0cc-4c18-88e3-b5797995ce10)

</p>
<p>
In powershell, ping 10.0.0.4
</p>
<br />

<p>
  
![Screenshot 2025-03-09 210409](https://github.com/user-attachments/assets/e29dc878-f6f3-4ee4-a84a-c28ae44c9b2f)

</p>
<p>
Observe the data packets. 
</p>
<br />

<p>
  
![Screenshot 2025-03-09 210527](https://github.com/user-attachments/assets/6a66b38b-90bb-4977-b1f1-9eee11641be8)

</p>
<p>
Type ipconfig /all
</p>
<br />

<p>
  
![Screenshot 2025-03-09 210628](https://github.com/user-attachments/assets/e42379ca-2f02-40b5-b9dc-e9ee1c4bbcb4)

</p>
<p>
Notice that the DNS Servers is sucessfully pointiing to dc-1.
</p>
<br />

<p>
  
![Screenshot 2025-03-09 210858](https://github.com/user-attachments/assets/12afcafb-592b-4ab3-845a-8d4de0c17506)

</p>
<p>
In Azure go back to virtual machines, select both vms, click on the three dots and stop the virtual machines so they don't continue to run.
</p>
<br />

<p>
  
![Screenshot 2025-03-09 210906](https://github.com/user-attachments/assets/2ffe8665-c0de-42a1-8f13-acf6bd63c886)

</p>
<p>
Select Yes.
</p>
<br />

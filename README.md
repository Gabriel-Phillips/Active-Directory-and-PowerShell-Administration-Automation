<h1>Active Directory and PowerShell Administration</h1>
Create User Accounts, Groups, and OUs // Delegate Administrative Tasks // Create and Link GPOs


<h2>Description</h2>

- Installed and configured Windows Server within VirtualBox environment for testing and development purposes.
- Implemented Active Directory Domain Services (AD DS), including promoting the server to a domain controller and configuring user accounts, groups, and organizational units (OUs).
- Utilized PowerShell cmdlets such as New-ADOrganizationalUnit, New-ADUser, New-ADGroup, Add-ADGroupMember, and Set-ADUser to automate user and group management tasks, improving efficiency and accuracy.
- Created and linked Group Policy Objects (GPOs) through the Group Policy Management console, applying security policies and settings to specific OUs.
- Edited GPO settings using the Group Policy Management Editor, ensuring alignment with organizational security requirements and standards.


<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b> 
- <b>Oracle VirtualBox</b>

<h2>Environments Used </h2>

- <b>Windows Server 2019</b>

<h2>Walk-Through:</h2>

<p align="left">
<strong>Step 1: Install Windows Server in VirtualBox</strong>

Download the ISO file for Windows Server from Microsoft's website.

Open VirtualBox and create a new virtual machine.

Mount the Windows Server ISO file as the installation media for the virtual machine.

Start the virtual machine and follow the on-screen prompts to install Windows Server.

- [Oracle VirtualBox](https://www.virtualbox.org/wiki/Downloads)
- [Windows Server 2019](https://www.microsoft.com/en-us/evalcenter/download-windows-server-2019)

<strong>Step 2: Install and Configure Active Directory Domain Services (AD DS)</strong>

Open Server Manager from the Start menu.

Click on "Add roles and features" and follow the wizard to install the Active Directory Domain Services role.

After installation, promote the server to a domain controller by running the Active Directory Domain Services Configuration Wizard.

<img src="https://i.imgur.com/fOuPgvQ.png" height="80%" width="80%" alt="1"/>

<strong>Step 3: Create User Accounts, Groups, and OUs</strong>

Open "Active Directory Users and Computers" from the Tools menu in Server Manager.

Right-click on the domain and select "New" to create new user accounts, groups, and organizational units (OUs).

<img src="https://i.imgur.com/Opro4pN.png" height="80%" width="80%" alt="2"/>
<img src="https://i.imgur.com/KfmyhWH.png" height="80%" width="80%" alt="3"/>
<img src="https://i.imgur.com/lI9zfZe.png" height="80%" width="80%" alt="4"/>
<img src="https://i.imgur.com/HNAHDET.png" height="80%" width="80%" alt="5"/>

<strong>Step 4: Delegate Administrative Tasks</strong>

Use PowerShell cmdlets like New-ADOrganizationalUnit, New-ADUser, New-ADGroup, Add-ADGroupMember, and Set-ADUser to automate user and group management tasks.

For example:

New-ADOrganizationalUnit -Name "Sales" -Path "OU=Departments,DC=domain,DC=com"

New-ADUser -Name "John Smith" -Path "OU=Sales,OU=Departments,DC=domain,DC=com"

New-ADGroup -Name "Sales Team" -GroupScope Global -Path "OU=Groups,DC=domain,DC=com"

Add-ADGroupMember -Identity "Sales Team" -Members "John Smith"

<img src="https://i.imgur.com/P8efutp.png" height="80%" width="80%" alt="7"/>
<img src="https://i.imgur.com/gC3v0x0.png" height="80%" width="80%" alt="8"/>
<img src="https://i.imgur.com/OwmozwY.png" height="80%" width="80%" alt="9"/>
<img src="https://i.imgur.com/CLkXLVc.png" height="80%" width="80%" alt="10"/>

<strong>Step 5: Group Policy Objects (GPOs)</strong>

Open "Group Policy Management" from the Tools menu in Server Manager.

Right-click on an OU and select "Create a GPO in this domain, and Link it here."

Edit GPO Settings:

Edit the GPO settings using the Group Policy Management Editor.

Configure policies and settings according to your organization's requirements.

<img src="https://i.imgur.com/HsP4xiZ.png" height="80%" width="80%" alt="11"/>
<img src="https://i.imgur.com/8zjbrD1.png" height="80%" width="80%" alt="12"/>
<img src="https://i.imgur.com/28HNm1a.png" height="80%" width="80%" alt="13"/>
<img src="https://i.imgur.com/bDSgtHv.png" height="80%" width="80%" alt="14"/>

By following these steps, you'll be able to successfully recreate your own Active Directory Management project, including installing and configuring Active Directory, creating user accounts, groups, and OUs, delegating administrative tasks, and managing Group Policy Objects (GPOs). Adjust the steps as needed based on your specific environment and requirements.

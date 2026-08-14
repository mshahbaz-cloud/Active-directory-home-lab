# Active-Directory-Home-Lab
Active Directory home lab built using Windows Server 2025 and VirtualBox. Configured a Domain Controller, Organizational Units, users, security groups and password policies.

## Overview
Built a Windows Server 2025 Active Directory environment using VirtualBox.

## Skills Demonstrated
- Active Directory
- Windows Server 2025
- User Management
- Security Groups
- Organizational Units (OUs)
- Group Policy
- Password Policies
 
## Tools Used
- VirtualBox
- Windows Server 2025 Evaluation
- Active Directory Domain Services (AD DS)
  
## Tasks Completed
- Installed Windows Server 2025
- Renamed Server to DC01
- Installed Active Directory Domain Services
- Promoted Server to Domain Controller
- Created company.local domain
- Created IT and HR organizational units
- Created users
- Created security groups
- Added users to groups
- Configured password policies

## Architecture

Windows Server 2025 (DC01)
├── Active Directory Domain Services (AD DS)
├── DNS Server
│
└── company.local
    │
    ├── IT OU
    │    ├── M Baz
    │    ├── Sarah Khan
    │    └── IT Staff Group
    │
    └── HR OU
         ├── David Brown
         └── HR Staff Group

## Network Diagram

Internet
│
▼
VirtualBox Host
│
▼
DC01 (Windows Server 2025)
│
├── Active Directory
├── DNS
├── Users
├── Groups
└── Group Policy

## What is a Domain Controller?
A Domain Controller (DC) is a Windows Server that authenticates users, authorises access to resources, and enforces security policies within an Active Directory domain.
In this project, DC01 was configured as the Domain Controller for the company.local domain.

## DNS Role in Active Directory
DNS is a critical component of Active Directory.
When users or computers attempt to log into the domain, DNS helps locate the Domain Controller and Active Directory services.
Without DNS, computers would be unable to locate domain resources and authentication services.

## OU vs Security Group
### Organizational Unit (OU)
An Organizational Unit is used to organise users, groups, and computers into logical containers.
Examples used in this project:
- IT
- HR

### Security Group
A Security Group is used to assign permissions and control access.
Examples used in this project:
- IT Staff
- HR Staff
  
### Key Difference
OUs provide organisation.
Security Groups provide access control and permissions.

## Authentication vs Authorization
### Authentication
Authentication verifies who a user is.
Example:
A user enters a username and password and Active Directory confirms their identity.
 
### Authorization
Authorization determines what a user is allowed to access after authentication has been completed.
Example:
A member of the IT Staff group may receive access to IT resources while HR users receive different permissions.

## Troubleshooting
### Problem
Windows Server installation displayed a black screen and would not boot correctly in VirtualBox.

### Investigation
Reviewed VirtualBox configuration settings and tested different boot configurations.

### Root Cause
The virtual machine was configured with UEFI settings that prevented the Windows Server installation media from booting correctly.

### Resolution
Disabled the UEFI boot option and restarted the virtual machine.
The Windows Server installation loaded successfully and the deployment continued without further issues.

## Testing
### Test 1 – Domain Verification
Verified that the company.local domain was successfully created and accessible through Active Directory Users and Computers.
Result: ✅ Passed

### Test 2 – User and OU Verification
Verified that the IT and HR Organizational Units were created and that user accounts were successfully added.
Result: ✅ Passed

### Test 3 – Security Group Verification
Verified that users were added to the correct security groups and group membership was displayed correctly.
Result: ✅ Passed

### Test 4 – Password Policy Verification
Verified that the minimum password length policy was configured to 10 characters through Group Policy Management.
Result: ✅ Passed

## What I Learned
- How to install and configure Windows Server 2025.
- How to deploy Active Directory Domain Services (AD DS).
- How to promote a server to a Domain Controller.
- How DNS integrates with Active Directory.
- How Organizational Units (OUs) are used to organise users and resources.
- How Security Groups are used to manage permissions and access.
- How Group Policy can enforce security settings across a domain.
- How to troubleshoot Windows Server deployment issues in a virtual environment.

## Future Improvements
- Deploy a Windows 11 client machine.
- Join the client to the company.local domain.
- Test domain logins using Active Directory accounts.
- Create additional Group Policy Objects (GPOs).
- Implement shared folders and NTFS permissions.
- Automate user management tasks using PowerShell.

## Screenshots
### 1. Windows Server Installed
<img width="1031" height="778" alt="01-Windows-Server-Installed" src="https://github.com/user-attachments/assets/40d3b00a-6703-4a79-b44c-3f8eaea6c07e" />

### 2. Server Renamed to DC01
<img width="1906" height="1016" alt="02-Server-Renamed-DC01" src="https://github.com/user-attachments/assets/0928dbc8-5fb4-4b9a-90ed-a5472353fb9e" />

### 3. Active Directory Domain Services Installed
<img width="1022" height="872" alt="03-ADDS-Installed" src="https://github.com/user-attachments/assets/a73884fa-ebce-46bf-90d5-435518f68a94" />

### 4. Domain Created
<img width="1917" height="1015" alt="04-Domain-Created" src="https://github.com/user-attachments/assets/bd8c0fd0-2d01-4d2e-8f60-94cca65cdbd5" />

### 5. Organizational Units Created
<img width="1018" height="867" alt="05-OU-Creation" src="https://github.com/user-attachments/assets/0ff94923-b188-4d28-9726-94f1c7a3c1d3" />

### 6. Users Created
<img width="1022" height="871" alt="06-Users-Created" src="https://github.com/user-attachments/assets/1a0544a7-7d81-4149-b6df-d2be39f8f4c5" />

### 7. Security Groups Configured
<img width="1022" height="872" alt="07-Security-Groups" src="https://github.com/user-attachments/assets/4736f2b4-83e4-409a-b1e7-75cced567c4c" />

### 8. Password Policy Configured
<img width="1022" height="870" alt="08-Password-Policy" src="https://github.com/user-attachments/assets/2c2719d1-4370-4e79-9b1f-84e913aec46c" />


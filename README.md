# Setting Up and Managing Office 365 for Small Business Operations

Objective: The goal of this homelab project is to simulate the deployment and management of Office 365 (now Microsoft 365) within a small business environment. This project will help you gain hands-on experience in setting up and configuring Office 365 services, managing users, securing data, and troubleshooting issues in a cloud-based environment.

Lessons Learned:

Cloud Admin Skills: Gained experience with Microsoft 365 Admin Center for user management and service configuration.
Security Best Practices: Implemented security measures such as MFA, conditional access, and data loss prevention.
Collaboration Tools Mastery: Set up Teams and OneDrive to improve team collaboration and file sharing.
PowerShell Proficiency: Gained hands-on experience automating tasks and managing Office 365 with PowerShell.
Backup & Recovery Knowledge: Learned about the importance of data backup and tested restoration methods.
Project Steps:

Tools
Office 365 Admin (30 Day free trial)

https://www.microsoft.com/en-us/microsoft-365/business/microsoft-365-business-standard-one-month-trial 

Office 365 Tenant Setup:

Sign up for a Microsoft 365 Business or Education trial.
Set up the tenant with your domain name (if you have one) or use the default domain.
Configure the basic tenant settings (language, region, etc.).

![image](https://github.com/user-attachments/assets/c7ec4ac2-6d22-455e-89ce-b96cb19c9871)

![image](https://github.com/user-attachments/assets/e0eae49d-2d67-403f-a680-43f2f913e07b)

User Management:

Create user accounts and assign appropriate licenses
Use the Microsoft 365 Admin Center to manage user roles and permissions. 
Set up security groups and dynamic groups for organizing users.

Created a sample of 10 users for the practical lab. Using Ava Johnson as an example. Got a brief overview of her account and noticed that some fields are not filled in yet but they will be later on in the exercise. 

![image](https://github.com/user-attachments/assets/90074413-224f-4657-aaa3-7cb361f855bf)

![image](https://github.com/user-attachments/assets/3a06cdd8-a725-410b-b4b5-a2ec5ca9f94c)

![image](https://github.com/user-attachments/assets/5bff372b-0970-4e6d-85b6-c3cd8ec4ef0b)

I've assigned her the default Microsoft 365 Business Standard licenses, 14 of 25. Scrolled through the licenses to makes sure that she is only assigned the licenses that she'll need for her role. In our case she'll be given Help Desk, Teams, and User Admin roles and permissions. There is an option too fine tune her roles but in this practice we're only gonna go w/ what is available under Admin center access and not "show all by category".

![image](https://github.com/user-attachments/assets/0c82b42d-1727-4bfc-9645-f24de63c388d)

To set up security groups we first go to "Active teams and groups" on the left hand of the page under "Teams & groups" section. From there we go to the security groups tap and click "add a security group" to make a new one. Name the security group "Help Desk" and click next then create group.

![image](https://github.com/user-attachments/assets/250f39ab-6666-4748-90f7-de2cca27dfe6)

![image](https://github.com/user-attachments/assets/e96576dd-4b2e-40df-a9ce-b012e6f120aa)

![image](https://github.com/user-attachments/assets/c755e724-3c77-4040-a17e-f88141c46418)

![image](https://github.com/user-attachments/assets/dd2f1eee-addc-4fdb-8c5e-99611ec1b6f9)

Email Setup (Exchange Online):

Configure mailboxes for the created users.
Set up custom email domains, configure mail flow rules, and test email communication.
Implement data loss prevention (DLP) policies and spam filtering.

To configure mailboxes for created users, we first go to the users section in the left-hand pane, select Users and then choose Active users. Select the user you want to configure the mailbox for, in our case it would be Ava Johnson. In the User details page, under Licenses and Apps, click apps on the bottom drop down section. Double check that the user is assigned the appropriate license that includes Exchange Online, which should be part of the Microsoft 365 Business Basic plan. After assigning the license, click Save to apply changes. The mailbox will be created automatically when the license is assigned. 

![image](https://github.com/user-attachments/assets/70da2423-a73d-411f-b73e-9975551629cc)

![image](https://github.com/user-attachments/assets/10c44270-2b27-4926-92f1-7e64a3e4923b)

To set up a custom email domain we need to go to Setup in the admin center. Under Domains, select Add domain to add your domain to Microsoft 365. For example, I'm using veridiontech.com as a domain name. Once the domain is verified, go back to Active users, select the user, and update their User name to use the new domain (i.e. veridiontech.com)

![image](https://github.com/user-attachments/assets/304596da-19f0-48f2-83de-1618723a4373)

![image](https://github.com/user-attachments/assets/4366acd1-3167-4bc7-91ad-55c5ed9e8b85)

![image](https://github.com/user-attachments/assets/82940a0d-1b69-4f54-9763-f97643ada643)

To configure mail flow rules (to filter emails, redirect them, or set up security protocols), go to Exchange Admin Center which is towards the bottom of the page on the left-hand pane. In the Exchange Admin Center, select Mail flow and then choose Rules. From here, you create new rules for email routing and other configurations like blocking externl mail.

![image](https://github.com/user-attachments/assets/e7b49e13-029d-4cdd-b1c6-9e86e743262e)

![image](https://github.com/user-attachments/assets/a5445678-0fe3-455c-8f70-86dd11f86fd5)

![image](https://github.com/user-attachments/assets/684b3b59-1ee0-46c1-aa4b-61faf19bf3bc)

![image](https://github.com/user-attachments/assets/55fbfd91-0074-45fb-a7e7-714668baf167)

To configure Data Loss Prevention (DLP) Policies we first go to the Security & Compliance center.

![image](https://github.com/user-attachments/assets/364c09c5-11b7-4029-a5d8-6dfb03028249)

Collaboration Setup (Teams & OneDrive):

Set up Microsoft Teams for internal communication and collaboration.
Create channels, configure settings, and test messaging and file sharing.
Set up OneDrive for Business for file storage and sharing, and implement access controls.

Security & Compliance:

Enable Multi-Factor Authentication (MFA) for users to secure accounts.
Implement conditional access policies to control access to Office 365 resources.
Set up Microsoft Defender for Office 365 to protect against threats like phishing.

PowerShell Automation:

Learn and execute basic PowerShell commands for Office 365 administration (user management, report generation, license assignment, etc.).
Automate repetitive tasks like creating user accounts, assigning licenses, and generating reports.

Backup and Restore:

Explore third-party backup solutions for Office 365 data (e.g., emails, SharePoint, OneDrive).
Test data restoration procedures to ensure recovery of lost files or emails.

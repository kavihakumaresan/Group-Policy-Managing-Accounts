<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Group Policy Management and Managing Accounts(Azure)</h1>
This tutorial outlines the how to do group policy management in Active Directory and How to enabling and unlocking accounts and resetting passwords .<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services

<h2>Operating Systems Used </h2>

- Windows Server 2022, at least 2vCPUs, 8GB RAM
- Windows 10 Pro (21H2), at least 2vCPUs, 8GB RAM

<h2>High-Level Deployment and Configuration Steps</h2>

- Create some users within the domain
- Configure group policy account lockout settings
- Enabling and disabling accounts
- Observing logs


<p>
<h3></h3>Creating Users in Active Directory and Configuring Group Policy:</h3> <br>
       Open Active Directory Users and Computers by searching for dsa.msc in the search bar.Navigate to _EMPLOYEES OU, right-click on it, and select New → User.
Fill in the required details, such as the username and password. Repeat this step to create multiple users.
</p>

![image](https://github.com/user-attachments/assets/fc1d7ce7-3f1b-4f47-9c03-c6115d86e63b)

<p>
<h4>Editing the Default Domain Policy to Configure Account Lockout Policy:</h4><br>
 Open the Group Policy Management Console (GPMC) by searching for gpmc.msc in the search bar.Locate and expand your domain, then click on Default Domain Policy (or another existing GPO if needed).Right-click on Default Domain Policy and select Edit.In the Group Policy Management Editor, navigate to:Computer Configuration → Policies → Windows Settings → Security Settings → Account Policies → Account Lockout Policy.Configure the account lockout settings as needed.
</p>

![image](https://github.com/user-attachments/assets/02bdccbe-821d-4bef-b692-5f69769dc8e2)

![image](https://github.com/user-attachments/assets/1ecaf8ff-bdc8-4f4b-bbfa-bbca118a5b5f)

<p>
<h5>Testing Account Lockout in Active Directory:</h5><br>
Log in to DC-1.Pick a user account from Active Directory that you created earlier.Enter the wrong password 10 times to trigger the account lockout.Check if the account is locked in Active Directory Users and Computers (dsa.msc).If you want to unlock the account,Right-click the user → Properties → Account tab → Unlock account → Apply & OK.If you want to reset the password,Right-click the user → Reset Password → Enter a new password → Confirm.Log in with the new password to verify access.
</p>

![image](https://github.com/user-attachments/assets/bcb99636-c8ce-4d34-b155-6c7e9df60f3d)


![image](https://github.com/user-attachments/assets/2f6f8c17-d7a7-47d4-a3f1-23af2d3f6e91)


![image](https://github.com/user-attachments/assets/ad79198c-83d2-4507-90e5-b3397af29ac6)


![image](https://github.com/user-attachments/assets/7f563a2c-8ef6-4834-a7df-96f8e24c6c6a)















</p>





 

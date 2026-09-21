<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Group Policy and Managing Accounts</h1>
This lab focuses on managing user accounts in an Active Directory (AD) environment. The lab demonstrates how account lockouts occur, how administrators can unlock accounts and reset passwords, how to disable and re-enable user accounts, and how to review security-related logs on both the Domain Controller and client machine.
These tasks are commonly associated with help desk, system administration, and cybersecurity roles.
  <br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
  

<h2>Operating Systems Used </h2>

- Windows Server 2025
- Windows 11 Pro (25H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Configure Account Lockout
- Test Account Lockout and Recovery
- Disable and Re-enable the Account
- Review Logs

<h2>Deployment and Configuration Steps</h2>

<p>
<img width="982" height="696" alt="image" src="https://github.com/user-attachments/assets/f1077cfe-f22c-4e47-a594-90ae69eb2ec4" />
</p>


- I first logged on to DC-1 and navigated to Group Policy Manager in order to configured the account lockout policy.
- The account lockout threshold determines how many unsuccessful authentication attempts can occur before the account is locked.
- This is an important account-security control because it can limit repeated authentication attempts.
- This is also needed to perform so of the task in the lab like testing account lockout and recovery. 
<br />

<p>
<img width="682" height="601" alt="image" src="https://github.com/user-attachments/assets/3ee9e5e0-3fbe-430b-a8a6-1a508ca3ca2b" />

</p>


- I then incorrectly entered in the wrong password on client-1 in order to show account lock out in action.
- Since I created a threshold in Group Policy Manager continuously entering in the wrong password does in fact lock the account.
  
<br />

<p>
<img width="1090" height="668" alt="Account Lockout" src="https://github.com/user-attachments/assets/784a0cf1-9244-427f-bdce-21f394402c9d" />

</p>


- I then logged back onto DC-1 and used Active Directory and saw that the account was in fact locked.
- In Active Directory I was also about to unlock the account, unlocking an account restores the account's ability to authenticate after an account lockout.
- This is a common type of account-management task that may be handled by an IT support technician or system administrator.
<br />

<img width="474" height="320" alt="image" src="https://github.com/user-attachments/assets/0b1a9859-28c0-45ea-8b66-69087817699e" />

- I also went ahead and change the user's password for security proposes.
- A password reset can restore a user's ability to authenticate when the existing password is unknown or needs to be replaced.

  

<img width="773" height="383" alt="image" src="https://github.com/user-attachments/assets/9025bcd0-c390-4341-961d-6579feb367ff" />


- I then try to relog into the test account after using Active Diretory to unlock the account.
- I was then able to use PowerShell and verify that I was on the correct test account.

<img width="634" height="468" alt="image" src="https://github.com/user-attachments/assets/ed586fcb-a800-4833-af6d-e58ac3e3a0a4" />

- I returned to Active Directory and disabled the same user account.
- Disabling an account prevents the account from being used to authenticate.
- This provides another important account-management control within Active Directory.

<img width="777" height="373" alt="image" src="https://github.com/user-attachments/assets/e62cd1fe-99a5-4fc7-8c75-809d99d0ab37" />

- I then attempted to log into the disabled account, and this demonstrates how disabling an account affects authentication.
- It also allows me to compare an account that is disabled with an account that was previously locked.


<img width="1210" height="917" alt="image" src="https://github.com/user-attachments/assets/4711a9b4-9641-4028-bde5-e6b194483ae0" />

- I then reenabled the account and logged back into client-1 to verify that it worked.


  <img width="1912" height="1057" alt="image" src="https://github.com/user-attachments/assets/297bc137-e220-45cd-9e5d-c59cfe099cfb" />


- I then went to Event Viewer to look at the logs of the login failures. I was able to see where the incorrect passwords were entered and when I put in the correct credentials.
- Reviewing logs can help administrators investigate authentication problems and understand what happened during an account-management event.

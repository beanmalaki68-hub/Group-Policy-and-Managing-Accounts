<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Active Directory Lab</h1>





https://github.com/user-attachments/assets/37bdc2dd-60b4-4a11-b520-889683383c0d



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
  

<h2>Operating Systems Used </h2>

- Windows Server 2025
- Windows 11 Pro (25H2)


# Frist Task - Creating Security Groups and added user to them

This lab demonstrates how to create and manage Security Groups in Active Directory Users and Computers (ADUC). I navigated to the domain, creating a new group, and configuring it as a Global Security Group. I then demonstrate opening a user's properties, selecting the Member Of tab, and adding the user to a security group such as GG-IT. This allows users to receive permissions based on their group membership instead of assigning permissions individually to each user.

<h2>Video Walkthrough</h2>

https://youtu.be/J1W1WHCb0-w



# Second Task - Creating a Network File

This lab demonstrates how to create and configure a network file share in an Active Directory environment. I created a Sales folder and configured it so members of the GG-Sales security group can access the shared resource. The folder is configured through its Sharing and Security properties, with permissions assigned to the appropriate security group. The video then verifies that the shared folder can be accessed from a client computer through the network.

<h2>Video Walkthorugh</h2>

https://youtu.be/jvmM0YUa9sw


# Third Task - Creating a Group Policy Object

This la demonstrated how Group Policy can be used to centrally manage Windows user settings across a domain. Instead of configuring every computer individually, an administrator can create a GPO and apply it to an OU so that the policy automatically affects the appropriate users or computers. The Restrict Control Panel example is useful in a business environment because administrators may want to prevent standard users from changing certain Windows settings. This can help maintain consistent configurations and reduce the possibility of users making changes that could create security or support issues.


<h2>Video Walkthrough</h2>

https://youtu.be/2nUxLISxjQw



# Fourth Task - Testing our Group Policy

This lab demonstrated how to force and verify Group Policy updates on a domain-joined Windows computer. The gpupdate /force command is useful when testing Group Policy because it tells Windows to immediately reprocess its Group Policy settings. This is especially helpful for administrators who have just created or modified a GPO and want to test the change without waiting for the normal Group Policy refresh cycle. The lab also showed the difference between configuring a GPO on the domain controller and testing the GPO from a client computer. The domain controller manages the policy, while the domain-joined client receives and processes the policy.


<h2>Video Walkthrough</h2>

https://youtu.be/9lQqYeIpwlU

<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket -  Post-Install Configuration</h1>
This tutorial outlines the post-installation configuration of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Microsoft Azure
- Virtual Machine
- osTicket 


<h2>Good Things to Know</h2>

- [Roles](https://docs.osticket.com/en/latest/Admin/Agents/Roles.html)
- [Departments](https://docs.osticket.com/en/latest/Admin/Agents/Departments.html)
- [Teams](https://docs.osticket.com/en/latest/Admin/Agents/Teams.html) 
- [Agents](https://docs.osticket.com/en/latest/Admin/Agents/Agents.html)
- [Users](https://docs.osticket.com/en/latest/Agent/Users/User%20Directory.html)
- [Service Level Agreement(SLA)](https://docs.osticket.com/en/latest/Admin/Manage/SLA%20Plans.html)
	
   

<h2>Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/gAXVBO2.png" height="70%" width="70%" alt="Login to osTicket"/>	
</p>

Copy this link to go to [osTicket](http://localhost/osTicket/scp/login.php) and login using your previously created credentials.

<img src="https://i.imgur.com/Jabe0zH.png" height="70%" width="70%" alt="Creating Super Admin Role"/>
<p>
Next, we will be creating roles in the "Admin Panel" for osTicket. Click the "Admin Panel" link at the top right to get started. If the link says "Agent Panel", then you are in the "Admin Panel".

- From Agents Tab > Roles > Add New Role
	- Name: Super Admin
	- From Permissions Tab: Tick every permission from the Tickets, Tasks, and Knowledgebase tabs
- Finally, Add That Role
</p>

<img src="https://i.imgur.com/sP2OpuV.png" height="70%" width="70%" alt="Creating System Administrators Department"/>
<p>
After creating the "Super Admin" role, we will be creating the "System Administrators" department

- From Agents Tab > Departments > Add New Department
	- Name: System Administrators
- Finally, press the "Create Dept" button
</p>


<img src="https://i.imgur.com/Jabe0zH.png" height="70%" width="70%" alt="Creating Super Admin Role"/>
<p>
Next, we will be creating roles in the "Admin Panel" for osTicket. Click the "Admin Panel" link at the top right to get started. If the link says "Agent Panel", then you are in the "Admin Panel".

- From Agents Tab > Roles > Add New Role
	- Name: Super Admin
	- From Permissions Tab: Tick every permission from the Tickets, Tasks, and Knowledgebase tabs
- Finally, Add That Role
</p>

<img src="https://i.imgur.com/StrMrvq.png" height="70%" width="70%" alt="Creating Level II Support Team"/>
<p>
Now, we will be creating a team. From the Agents Tab > Teams Tab, you will notice that theres a "Level I Support" team. We will be creating a "Level II Support" team. 

- From Agents Tab > Teams > Add New Team
	- Name: Level II Support
- From the Members tab, add yourself in the Select Agent dropdown menu and click "Create Team". In this tutorial, I added "User Admin".
</p>


<img src="https://i.imgur.com/6mMaTXw.png" height="70%" width="70%" alt="Allowing Tickets To Be Created By Anyone"/>
<p>
After these configuration steps, we will now set it such that anyone is allowed to create tickets.

- From Settings Tab > User Tab
	- Ensure that "Registration Required" checkbox is UNCHECKED
</p>

<img src="https://i.imgur.com/YJsRxNp.png" height="70%" width="70%" alt="Creating Jane.Doe Agent"/>
<p>
Now we will be configuring agents.

- From Agents Tab > Add New Agent
- Create an agent with these credentials
	- Name: Jane Doe
	- Email: jane.doe@osticket.com
	- Username: jane.doe
	- Set Password: Password1
		- Untick the "Send the agent a password reset email" and "Require password change at next login" checkboxes 
<img src="https://i.imgur.com/IJGJs5S.png" height="70%" width="70%" alt="Adding Access and Teams"/>
	
- From the Access Tab in the Add New Agent form, add the following access
	- Primary Department: System Administrators
	- Role: Super Admin
	- Extended Access: Support
	- Extended Access Role: Super Admin
- After that, select the "Teams" tab and add the "Level II Support" team
- Finally, hit the Create button
</p>

<img src="https://i.imgur.com/fGso8Oo.png" height="70%" width="70%" alt="Creating Agent John Doe"/>
<p>
Next, following the same steps, we will be creating John.
	
- From the steps from creating Jane's account, create an Agent with the following credentials:
	- Name: John Doe
	- Email: john.doe@osticket.com
	- Username: john.doe
	- Password: Password1
	- Primary Department: Support
	- Role: All Access
- After that, hit "Create"
</p>

<img src="https://i.imgur.com/FdHL3zC.png" height="70%" width="70%" alt="Creating Users"/>
<p>
Now, we will be creating Users that will send tickets.
	
- From Agent Panel > Users Tab > Add User. Create a Users with the following credentials:
	- User 1
		- Email: karen@osticket.com
		- Full Name: Karen Karen
	- User 2
		- Email: ken@osticket.com
		- Full Name: Ken Ken
- After entring the credentials, hit "Add User" 
</p>

<img src="https://i.imgur.com/8hnGzzD.png" height="70%" width="70%" alt="Creating Service Level Agreements"/>
<p>
After configuring the users, we will be creating Service Level Agreements (SLA)
	
- From Admin Panel > Manage > SLA > Add New SLA Plan. Create the following SLA Severity Levels
	- Severity A
		- Name: SEV-A
		- Grace Period: 1
		- Schedule: 24/7
	- Severity B
		- Name: SEV-B
		- Grace Period: 4
		- Schedule: 24/7
	- Severity C
		- Name: SEV-C
		- Grace Period: 8
		- Schedule: Monday-Friday
- After entring a Service Level Agreement, hit "Add Plan" before creating your next SLA.
</p>

<img src="https://i.imgur.com/m6PLaAH.png" height="70%" width="70%" alt="Creating Help Topics"/>
<p>
Finally, we will be creating Help Topics
	
- From Admin Panel > Manage > Manage > Help Topics > Add New Help Topic. Create the following help topics
	- Business Critical Outage
	- Personal Computer Issues
	- Equipment Request
	- Password Reset
- After creating a help topic, hit the "Save Changes" button before moving onto creating the next help topic
</p>

<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />

<!-- 
<h2>Video Demonstration</h2>

- ### [YouTube: How To Configure osTicket, post-installation](https://www.youtube.com)
 -->

<h2>Environments and Technologies Used</h2>

- Oracle VM VirtualBox
- Debian
- Terminal
- Apache
- MariaDB

<h2>Operating Systems Used </h2>

- Debian 12.7.0

<h2>Post-Install Configuration Objectives</h2>

- Configuring **Roles**, **Departments**, and **Teams**
- Configuring ticket creation rules and permissions
- Creating agents and users
- Configuring a **Service Level Agreement (SLA)**
- Creating **Help Topics**

<h2>Configuration Steps</h2>

<h3>Part 1 - Accessing Our Ticketing System</h3>

In the last tutorial, we installed the prequisites needed to run  osTicket. We installed Apache, MariaDB, and PHP, and configured these services to work together. We gave our site the domain name `myhelpdesk.com`. Now that we have setup osTicket, we can begin configuring our ticketing system. Navigate to `myhelpdesk.com/scp/admin.php` to login with our admin credentials we created.

`Username: jay`

`Password: Password1`

We can now begin the post-installation configuration.

<h3>Part 2 - Configuring Role</h3>

To create a role, navigate to `Agents -> Roles -> Add New Role`.

<img src="images/CreateRole_1.png" />

We will give this role the name `Supreme Admin`.

<img src="images/CreateRole_2.png" />

To assign permissions for this role, go to the permissions tab.

<img src="images/CreateRole_3.png" />

As the name of this role implies, any user with this role should be given the most permissions. Go ahead and tick all the options in each of the sub tabs.

<img src="images/CreateRole_4.png" />

<img src="images/CreateRole_5.png" />

<img src="images/CreateRole_6.png" />

Click `Add Role`. We should now see this new role on the `Roles` page.

<img src="images/CreateRole_7.png" />

<h3>Part 3 - Configure Department</h3>

To create a new department, navigate to `Agents -> Departments -> Add New Department`.

<img src="images/CreateDepartment_1.png" />

We will call this department `System Administrators`. Leave all other settings as they are.

<img src="images/CreateDepartment_2.png" />

We will add agents to this department later. For the time being, click `Create Dept`. We should now see the department in the list of all departments.

<img src="images/CreateDepartment_3.png" />

<h3>Part 4 - Configure Team</h3>

A team allows us to manage agents from different departments. To create a team, navigate to `Agents -> Teams -> Add New Team`.

<img src="images/CreateTeam_1.png" />

In a real help desk environment, their will be different ticket escalation levels. As there is already a team for `Level I Support`, let's create a team for `Level II Support`.

<img src="images/CreateTeam_2.png" />

Again, we will add members to this team later. For now, create the team as is. We should now see the team in the list of all teams.

<img src="images/CreateTeam_3.png" />

<h3>Configuring Ticket Creation</h3>

In our help desk, anyone should be able to submit a ticket, whether they be a user, guest, agent, or admin.
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
- Configuring a Servive Level Agreement (SLA)
- Creating **Help Topics**

<h2>Configuration Steps</h2>

<h3>Part 1 - Accessing Our Ticketing System</h3>

In the last tutorial, we installed the prequisites needed to run  osTicket. We installed Apache, MariaDB, and PHP, and configured these services to work together. We gave our site the domain name `myhelpdesk.com`. Now that we have setup osTicket, we can begin configuring our ticketing system. Navigate to `myhelpdesk.com/scp/admin.php` to login with our admin credentials we created.

`Username: jay`

`Password: Password1`

We can now begin the post-installation configuration.

<h3>Part 2 - Configuring Roles</h3>

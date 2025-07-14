<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Post-Install Configuration Objectives</h2>

- Roles
- Departments
- Teams
- Agents
- Users
- SLA
- Help Topics

  <h2>Accessing osTicket</h2>
After completing the installation, you can access osTicket through the following URLs:

Admin / Analyst Login Page:
http://localhost/osTicket/scp/login.php
Use this link to log in as an administrator or help desk agent to manage tickets, settings, and users.

End User Support Portal:
http://localhost/osTicket
This is the public-facing portal where users can submit and check the status of their support tickets.

<h2>Configuration Steps</h2>

Step 1: Set Up System Settings

(Defines global help desk info, default email, and timezone)

Go to: Admin Panel → Settings → System

Configure:

- Helpdesk Name

- Default System Email

- Timezone

Click Save Changes

Step 2: Configure Email Addresses

(Sets up the addresses used to send/receive tickets and notifications)

Go to: Admin Panel → Emails

Click Add New Email

Add:

Email address (e.g., support@example.com)

Name

Assign it as the default system email if needed
<img width="936" height="843" alt="Screenshot 2025-07-10 at 7 04 00 PM" src="https://github.com/user-attachments/assets/1e63f024-fef7-41ed-95d1-99430dcee952" />
<img width="939" height="844" alt="Screenshot 2025-07-10 at 7 04 14 PM" src="https://github.com/user-attachments/assets/667aa490-8946-4f95-aaf2-5f7c792451a7" />

Step 3: Create Departments

(Groups tickets and agents by area of responsibility)

Go to: Admin Panel → Agents → Departments

Click Add New Department

Fill out:

Name (e.g., Tech Support, Billing)

Optional email

Optional department manager

Save changes
<img width="935" height="843" alt="Screenshot 2025-07-10 at 7 06 20 PM" src="https://github.com/user-attachments/assets/622a13f0-c128-434f-9984-2b2eed7d60d0" />
<img width="931" height="845" alt="Screenshot 2025-07-10 at 7 07 20 PM" src="https://github.com/user-attachments/assets/0e8bfe9a-2c73-443d-bcf2-b6f17fa482d5" />

Step 4: Define Roles (Permissions)

(Controls what agents can do based on their assigned level)

Go to: Admin Panel → Agents → Roles

You can:

Edit default roles (Admin, Staff, etc.)

Click Add New Role to customize:

Ticket access

Admin privileges

Visibility

💡 Example roles:

Staff – View/respond to tickets

Manager – Assign/reassign, limited config access

Admin – Full control
<img width="936" height="838" alt="Screenshot 2025-07-10 at 7 14 28 PM" src="https://github.com/user-attachments/assets/ae5c00f5-0ae6-4909-b685-c08f3fcd2d93" />

Step 5: Configure Teams

(Groups agents together to work on shared tickets.)

Go to: Admin Panel → Agents → Teams

Click Add New Team

Set:

Team Name (e.g., Tier 1 Support)

Assign agents to the team

Optional: assign a Team Lead

Save the team

💡 You can assign tickets to teams instead of individuals.
<img width="938" height="838" alt="Screenshot 2025-07-10 at 7 31 59 PM" src="https://github.com/user-attachments/assets/edece165-0884-4ea2-8355-60e5d4006ae5" />

Step 6: Add Agents (Support Staff)

(Adds staff who will log in and handle tickets.)

Go to: Admin Panel → Agents → Agents

Click Add New Agent

Enter:

- Full name

- Username

- Email address

Assign:

- Role

- Department

- Team (optional)

- Click Create Agent
<img width="933" height="844" alt="Screenshot 2025-07-10 at 7 16 35 PM" src="https://github.com/user-attachments/assets/48baf88a-551c-4cd6-b3d1-8b9b82afd550" />

Step 7: Add Help Topics

(Helps users categorize issues when submitting tickets)

Go to: Admin Panel → Manage → Help Topics

- Click Add New Help Topic

Example topics:

- Account Support

- Website Issue

- Billing Error
- <img width="938" height="838" alt="Screenshot 2025-07-10 at 7 12 59 PM" src="https://github.com/user-attachments/assets/ba6d3d5a-a876-491f-ab30-4033c44e8b83" />

Step 8: Create Users 

(Adds real or test users to submit tickets)

Go to: Admin Panel → Users → Add New User

Input:

Name

Email

Click Add User

💡 These users can now submit tickets via the client portal or email.
<img width="935" height="842" alt="Screenshot 2025-07-14 at 3 06 28 PM" src="https://github.com/user-attachments/assets/9809c995-067c-4350-b623-4e4b88e77fba" />

Step 9: Submit a Test Ticket

(Verifies ticket submission works correctly)

Go to: http://localhost/osTicket/

Submit a ticket using the test user's info

Select a help topic and describe the issue
<img width="930" height="837" alt="Screenshot 2025-07-10 at 7 19 51 PM" src="https://github.com/user-attachments/assets/e9a9d3e8-844b-409f-8d52-f5d7d80969c4" />

Step 10: Respond to the Ticket as an Agent

(Confirming that agents can reply and that the system functions end-to-end)

Log into the Admin Panel

Go to: Tickets → Open

Open the test ticket

Add a Response or Internal Note

Click Post Reply
<img width="935" height="839" alt="Screenshot 2025-07-10 at 7 27 19 PM" src="https://github.com/user-attachments/assets/b5d762ac-d2df-447f-aa44-03583146f3dd" />


Step 11: Configure SLA Plans 

(Defines how fast tickets must be responded to or resolved)

Go to: Admin Panel → Manage → SLA Plans

Click Add New SLA Plan

Set:

- Plan Name (e.g., "24hr Response")

- Response time expectations

- Grace periods

- Save

💡 SLAs can be assigned to help topics or departments.
<img width="938" height="842" alt="Screenshot 2025-07-14 at 3 07 39 PM" src="https://github.com/user-attachments/assets/403d4fb5-c7ab-4751-aa27-2af128e9a179" />


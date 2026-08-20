# 💻 Enterprise HelpDesk (Jira Service Management Project)

## 📌 Project Overview
This repository contains the design, implementation, and configuration documentation of an enterprise-level **IT Service Management (ITSM)** system built inside **Jira Service Management (JSM)**. This project replicates live L1/L2 IT Support and Desktop Support operations, focusing on service catalog deployment, incident tracking, and workflow automation.

---

## 🏗️ Project Architecture & Implementation

### 1. Customer-Facing Service Portal (Front-End)
* **Categorized Help Center**: Deployed an online customer portal structured with dedicated IT service request categories (Computers, Applications, Login Accounts).
* **Data-Driven Intake Forms**: Configured standardized request types for high-frequency IT issues:
  * **Laptop & Hardware Support**: Custom form layout to enforce corporate asset tracking.
  * **Software & Application Access**: Integrated baseline justification parameters.
  * **Account & Password Lockout**: Configured high-visibility intake fields for quick identification.

*📸 **Project Setup & Base Template Configuration:***
![Jira Space Creation](screenshots/jira-creat-space.png)

![Jira Template Selection](screenshots/basic-it-sevice-management-template.png)

![IT Form Fill Up Simulation](screenshots/it-service-create-form-fill-up.png)

*📸 **Customized Support Catalogs & Requests(Portal for user reqest):***
![Laptop & Hardware Support Catalog](screenshots/portal.png)

![Laptop & Hardware Support Catalog](screenshots/laptop-and-hardware-support.png)
![Software & Application Access Request](screenshots/Software%20&%20Application%20Access.png)
![Account & Password Lockout Form](screenshots/Account%20&%20Password%20Lockout.png)

![Account & Password Lockout Form](screenshots/MONITOER.png)

![Account & Password Lockout Form](screenshots/broken-keyboard.png)

![Account & Password Lockout Form](screenshots/batry-issue.png)

![Account & Password Lockout Form](screenshots/adobe-pro-installation.png)

![Account & Password Lockout Form](screenshots/slack-cyber-adit.png)

![Account & Password Lockout Form](screenshots/zoom-meeting.png)


---

### 2. Incident Management & Queue Configuration (Back-End)
* **Ticket Lifecycle Tracking**: Structured a 4-stage operational workflow (`Waiting for Support` ➔ `In Progress` ➔ `Pending Customer` ➔ `Done`) to track issues from ingestion to closure.
* **Optimized Agent Queues**: Built isolated queues to separate regular service requests from high-priority incident tickets, reducing manual dispatch overhead.
* **Production Simulation**: Logged and processed simulated tickets (e.g., *Laptop Screen Flickering* & *VPN Access Requests*) to validate end-to-end diagnostic resolution paths.

*📸 **Live Ticket Simulation & Queue Tracking:***

![First Ticket Generation Overview](screenshots/open.png)
![Central Queues Tracking](screenshots/queue.png)
![All Live Active Tickets](screenshots/10_All_Live_Tickets.png)
![Successful Lifecycle Ticket Resolution](screenshots/11_Ticket_Resolved.png)

---

### 3. Advanced Jira Work Management Automations (Production-Grade Rules)

Here is the functional logic and visual proof of the custom automation workflows built into the system to minimize manual IT dispatch overhead:

* **Account Lockout Auto-Assignment**: Set up an immediate route to auto-assign all incoming 'Password' or 'Lockout' tickets to the active technician.
* **VIP / Manager Escalation**: Upgrades a ticket to `Highest Priority` if keywords like *Manager*, *Urgent*, or *CEO* are detected.
* **Hardware Team Dispatcher**: Configured automated email notifications to inventory personnel (`tech@store.com`) whenever asset replacements are triggered.
* **Automatic Customer Response**: Deployed an instant system-generated comment on new tickets to communicate initial expectations.
* **Hardware Asset ID Mandate**: Moves a ticket to `Waiting for Customer` status if the *Asset ID* field is left empty during submittal.
* **Automated CSAT Survey Dispatch**: Automatically emails a satisfaction survey to the user the exact second a ticket is marked `Done`.
* **Dynamic Ticket Reopening**: Moves a closed ticket back to `In Progress` if a customer posts a follow-up comment.
* **Urgent Alert for Aging Tickets**: Daily morning sweep that places an escalation flag on any item stuck in `In Progress` for more than 5 days.

*📸 **Core Automations Architecture Map:***
![Jira Automation Flow Mapping](screenshots/12_Final_Automation_Flow.png)

---

## 💡 Technical Core Competencies Demonstrated
* **ITSM Framework**: Hands-on management of incidents vs. service requests under standard operational guidelines.
* **Jira Administration**: Practical proficiency in request schemas, custom field validation, status transitions, and administrative diagnostics.
* **Automation Engineering**: Deep utilization of complex conditional logic (When ➔ If ➔ Then) to optimize IT department overhead.

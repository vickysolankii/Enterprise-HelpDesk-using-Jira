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

### 2. Incident Management & Queue Configuration (Back-End)
* **Ticket Lifecycle Tracking**: Structured a 4-stage operational workflow (`Waiting for Support` ➔ `In Progress` ➔ `Pending Customer` ➔ `Done`) to track issues from ingestion to closure.
* **Optimized Agent Queues**: Built isolated queues to separate regular service requests from high-priority incident tickets, reducing manual dispatch overhead.
* **Production Simulation**: Logged and processed simulated tickets (e.g., *Laptop Screen Flickering* & *VPN Access Requests*) to validate end-to-end diagnostic resolution paths.

### 3. Service Level Agreement (SLA) Controls
* **Resolution Deadlines**: Configured built-in SLA timers to manage resolution thresholds.
* **Priority Alignment**: Established fast-response lanes for critical connectivity and access blockages, while maintaining standard fulfillment tracks for software deployments.

### 4. Advanced Jira Work Management Automations (10 Production-Grade Rules)
* **Rule 1: Account Lockout Auto-Assignment**: Set up an immediate route to auto-assign all incoming 'Password' or 'Lockout' tickets to the active technician.
* **Rule 2: VIP / Manager Escalation**: Engineered a conditional branch that automatically upgrades a ticket to `Highest Priority` if keywords like *Manager*, *Urgent*, or *CEO* are detected.
* **Rule 3: Inactive Ticket Cleanup**: Formulated a daily cron-schedule trigger to auto-close stale tickets stuck in customer-pending status for more than 3 days.
* **Rule 4: Hardware Team Dispatcher**: Configured automated email notifications to inventory personnel (`tech@store.com`) whenever asset replacements are triggered.
* **Rule 5: Automatic Customer Response**: Deployed an instant system-generated comment on new tickets to communicate initial expectations and boost Customer Satisfaction (CSAT).
* **Rule 6: Hardware Asset ID Mandate**: Programmed a validator rule that flags a ticket and moves it to `Waiting for Customer` status if the *Asset ID* field is left empty during submittal.
* **Rule 7: Specialized Routing for Applications**: Built a classifier rule that detects complex software provisioning tickets and routes them away from general L1 to the dedicated Applications Support Queue.
* **Rule 8: Automated CSAT Survey Dispatch**: Configured a lifecycle trigger that automatically emails a structured feedback and satisfaction survey to the user the exact second a ticket is marked `Done`.
* **Rule 9: Dynamic Ticket Reopening**: Engineered a condition rule that automatically moves a closed or resolved ticket back to `In Progress` if a customer posts a follow-up comment.
* **Rule 10: Urgent Alert for Aging Tickets**: Built a daily morning routine trigger that sweeps the database and places an escalation flag on any item stuck in `In Progress` for more than 5 days.

---

## 💡 Technical Core Competencies Demonstrated
* **ITSM Framework**: Hands-on management of incidents vs. service requests under standard operational guidelines.
* **Jira Administration**: Practical proficiency in request schemas, custom field validation, status transitions, and administrative diagnostics.
* **Automation Engineering**: Deep utilization of complex conditional logic (When ➔ If ➔ Then) to optimize IT department overhead.

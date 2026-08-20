# 💻 Enterprise HelpDesk (Jira Service Management Portfolio Project)

## 📌 Project Overview
This project demonstrates a production-ready **IT Service Management (ITSM)** ticketing ecosystem built inside **Jira Service Management (JSM)**. Designed to simulate real-world L1/L2 IT Support Engineer workflows, this service desk manages user hardware requests, software access provisioning, and urgent account/password issues for an organization.

---

## 🌟 Key Features Implemented

### 1. Unified Customer Help Center
* Designed user-friendly Request Types mapped under specific IT catalog categories (Computers, Applications, Login Accounts).
* Embedded custom Description templates to mandate critical data collection (e.g., Asset ID, Software Justification, Locked Username) straight from the end-user.

### 2. ITIL-Aligned Ticketing Workflows
* Engineered lifecycle transitions for incoming support items: `Waiting for Support` ➔ `In Progress` ➔ `Pending Customer` ➔ `Done`.
* Structured dedicated Agent Queues to auto-segregate urgent login lockouts from hardware replacements.

### 3. Advanced Jira Automation Rules (Smart Operations)
* **Auto-Assignment Flow**: Programmed an instant route to auto-assign all incoming 'Password Reset' or 'Account Lockout' tickets to the active IT engineer.
* **VIP & Manager Escalation**: Configured condition alerts that automatically elevate ticket priority to `Highest` if the summary matches keywords like *Manager*, *Urgent*, or *CEO*.
* **Queue Cleanup (SLA Timer)**: Deployed daily checks to automatically resolve stale tickets stuck in customer-pending states after 3 days of inactivity.
* **Hardware Store Alerts**: Set up auto-email dispatchers (`tech@store.com`) whenever a user submits a laptop or equipment replacement query.
* **SLA First Response Greeting**: Created instant automated greeting comments on newly generated items to assure users their issue is being reviewed.

---

## 💡 Interview Talking Points (What I Learned)
* **ITSM & ITIL Basics**: Gained hands-on experience handling real incidents, service requests, and categorization principles.
* **Jira Administration**: Learned how to configure request types, manage hidden fields, read active queues, and streamline agent-to-customer communications.
* **SLA Awareness**: Understood the importance of prioritizing urgent business operational blockages over standard hardware deployments.

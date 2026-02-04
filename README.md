# Inbound Marketing Funnel – Lead Scoring & Routing

## 📌 Project Overview
This project is an automated lead-management system built in **Zapier**. It is designed to bridge the gap between marketing and sales by automatically identifying, scoring, and routing leads based on their business value.

### 🚀 Key Features
- **Real-Time Capture:** Instantly pulls data from Google Forms.
- **Intelligent Scoring:** Uses a custom Lookup Table to weight leads by job role.
- **Automated Enrichment:** Uses Apollo to find prospect details for high-value leads.
- **Dynamic Routing:** Sends "Hot Leads" to Pipedrive CRM and "Nurture Leads" to Google Sheets.

---

## 🛠️ The Workflow Architecture

### 1. Trigger: Google Forms
- **Action:** New Form Response  
- **Implementation:** Captures the lead's name, email, and job role to kick off the automation instantly.

### 2. Logic: Formatter by Zapier (Utilities)
- **Action:** Lookup Table  
- **Implementation:** Implemented as the "brain" of the flow. Assigns numeric values to roles (e.g., Founder = 50, Individual = 5).

### 3. Branching: Paths
- **Action:** Conditional Logic  
- **Implementation:** Leads with a score over 40 are routed to the Sales Path, while others go to the Nurture Path.

### 4. Path A: Sales Execution (High-Value)
- **Apollo integration:** Finds prospect's LinkedIn/persona data  
- **Pipedrive integration:** Creates a new Lead and Deal in CRM  
- **Gmail Notification:** Sends instant alert to sales team

### 5. Path B: Marketing Nurture (Low-Value)
- **Google Sheets integration:** Stores leads in structured format  
- **Data Integrity:** Uses headers (Name, Email, Score) to keep data clean for future campaigns

---https://docs.google.com/forms/d/e/1FAIpQLSec2nVRAdlmrEeQYL8Sji0GGR-8erah7Ut0mWvmS5PM04RJIw/viewform?usp=sharing&ouid=100520228213249022453



<img width="536" height="907" alt="image" src="https://github.com/user-attachments/assets/80803b04-95ed-47d8-ad3d-1d2dfd64add4" />


<img width="837" height="716" alt="image" src="https://github.com/user-attachments/assets/26a3efe2-35cd-43ed-b10e-e57d0839846d" />


<img width="1165" height="425" alt="image" src="https://github.com/user-attachments/assets/117e5afa-89db-4480-a732-3923993c449c" />


## 🧩 Tools Used
- Zapier
- Google Forms
- Formatter by Zapier
- Apollo
- Pipedrive
- Google Sheets

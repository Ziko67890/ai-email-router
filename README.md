# 📩 NexaFlow — AI Email Classification & Routing System

> Stop sorting emails manually. This n8n workflow uses GPT-4 to read every incoming email, classify it by department and priority, auto-reply to the sender, and route it to the right team — all in seconds.

**TSAcademy · AI Automation · Phoenix Cohort · Capstone Project**

---

## 💡 The Problem It Solves

Businesses receive hundreds of emails daily — sales enquiries, customer complaints, HR applications, finance requests. Manually reading, sorting, and forwarding each one wastes time and leads to missed messages. This system eliminates that entirely with AI.

---

## ⚡ What It Does

- 📥 Monitors the Gmail inbox every minute for new emails
- 🤖 Uses GPT-4 to classify each email — assigns a department, priority level, confidence score, and reasoning
- ↩️ Instantly sends an auto-reply to the sender confirming their message was received and routed
- 📊 Logs every email — sender, subject, body, classification, priority, confidence — to Airtable
- 📨 Forwards a beautifully formatted notification email to the correct department team
- 🚨 Detects angry customer emails and flags them with a special escalation alert
- 📺 Includes a live dashboard accessible via webhook to view all logged emails

---

## 🏢 Departments Supported

| Department | Type of Emails |
|---|---|
| 💼 **Sales** | Product enquiries, pricing, partnerships |
| 🎧 **Customer Service** | Complaints, support requests, angry customers |
| 👥 **HR** | Job applications, employee matters |
| 💰 **Finance** | Invoices, billing, payment queries |
| ⚙️ **Operations** | Logistics, internal processes, workflow issues |
| 📁 **Other** | Anything that doesn't fit a category |

---

## 🛠️ Tech Stack

| Tool | Role |
|---|---|
| **n8n** | Workflow automation engine |
| **Gmail** | Email trigger, auto-reply, and department notifications |
| **GPT-4** | AI classification — department, priority, confidence, and reason |
| **Airtable** | Email log database and live dashboard data source |

---

## 🚀 Getting Started

1. Import `Email_Classification.json` into your n8n instance via **Workflows → Import from file**
2. Connect your Gmail account via OAuth2 in n8n credentials
3. Add your OpenAI API key to n8n credentials
4. Add your Airtable Personal Access Token and update the base ID and table ID to match your setup
5. Replace the hardcoded department email address with your real team email addresses in each routing node
6. Activate the workflow and watch your inbox get sorted automatically

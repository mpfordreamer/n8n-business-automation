# 🤖 n8n Business Automation Workflows

![n8n](https://img.shields.io/badge/n8n-Workflow-orange?style=for-the-badge&logo=n8n)
![Status](https://img.shields.io/badge/Status-Active-green?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)

A comprehensive collection of **n8n workflows** designed to automate critical business processes, community management, and customer engagement. This repository serves as a centralized hub for automation scripts covering **Telegram**, **Discord**, and **WhatsApp** (Property Management).

## � Table of Contents
- [About the Project](#about-the-project)
- [📂 Repository Structure](#-repository-structure)
- [⚡ Workflow Details](#-workflow-details)
  - [Telegram Membership](#1-telegram-membership-automation)
  - [Discord Community](#2-discord-community-management)
  - [Property Automation](#3-property-automation-wa)
- [🛠️ Prerequisites](#️-prerequisites)
- [🚀 Installation & Setup](#-installation--setup)
- [⚠️ Security Note](#️-security-note)

---

## About the Project
This project provides ready-to-deploy automation solutions for businesses managing large communities or customer bases. By leveraging n8n, these workflows eliminate manual tasks such as user verification, role assignment, and lead follow-ups.

## 📂 Repository Structure
```
n8n-business-automation/
├── membership tele/           # Telegram automation workflows
├── membership discord/        # Discord management workflows
├── property automation wa/    # Real estate/Property WhatsApp automation
└── README.md
```

## ⚡ Workflow Details

### 1. Telegram Membership Automation
**Path:** `membership tele/n8n-telegram-membership.json`

Automate your private Telegram group management.
- **Auto-Join Approvals:** Automatically approves or denies join requests based on payment status or internal database checks.
- **Subscription Management:** Monitors user subscription validity and kicks/bans users upon expiration.
- **Broadcasts:** (Optional) Dispatch messages to valid members.

### 2. Discord Community Management
**Path:** `membership discord/`

A suite of workflows to manage a thriving Discord server.
- **Registration (`n8n-discord-registration.json`):** Onboards new users, syncing their Discord ID with your CRM or Google Sheets.
- **Role Sync (`n8n-discord-role-check.json`):** Periodically checks external databases (e.g., membership site) to assign or remove VIP roles.
- **Membership Status (`n8n-discord-membership.json`):** Handles logic for paid vs. free tier access and channel visibility.

### 3. Property Automation (WA)
**Path:** `property automation wa/property_reactivation.json`

Re-engage cold leads in the real estate sector using WhatsApp automation.
- **Lead Reactivation:** Scans your "Leads" database (Google Sheets/Airtable) for cold contacts.
- **Personalized Outreach:** Sends personalized WhatsApp messages (via WAHA or similar API) to inquire about interest.
- **Status Updates:** automatically updates the lead status based on replies (e.g., "Interested", "Stop", "Follow-up").

## �️ Prerequisites
Before importing these workflows, ensure you have:
- **n8n Instance:** A self-hosted or cloud version of [n8n](https://n8n.io/).
- **Connected Accounts:**
  - Telegram Bot Token
  - Discord Bot Token
  - Google Sheets (Service Account)
  - WhatsApp API Service (e.g., WAHA, Twilio)

## 🚀 Installation & Setup
1. **Clone the Repository:**
   ```bash
   git clone https://github.com/mpfordreamer/n8n-business-automation.git
   ```
2. **Import to n8n:**
   - Open your n8n dashboard.
   - Click **"Add Workflow"** > **"Import from File"**.
   - Select the desired `.json` file from the cloned folder.
3. **Configure Nodes:**
   - Double-click nodes with errors (marked red).
   - Select your own **Credentials** for each service (Telegram, Discord, etc.).
   - Update IDs (Channel ID, Sheet ID) to match your environment.

## ⚠️ Security Note
**All credentials have been sanitized.**
These JSON files do **not** contain API keys, passwords, or tokens. You must select your own credentials within your n8n instance after importing.

---
*Maintained by [mpfordreamer](https://github.com/mpfordreamer)*

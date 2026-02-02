# n8n Business Automation Workflows

This repository contains a collection of n8n workflows designed to automate various business processes, communities, and property management tasks.

## 📂 Project Structure

### 1. Telegram Membership Automation (`membership tele`)
Automates the management of Telegram group memberships.
- **Features:**
    - Handles user join requests.
    - Manages subscription status or access rights.

### 2. Discord Community Management (`membership discord`)
Comprehensive workflows for managing a Discord community.
- **Workflows:**
    - `n8n-discord-registration.json`: Handles new user registration.
    - `n8n-discord-membership.json`: Manages ongoing membership status.
    - `n8n-discord-role-check.json`: Automates role assignment and validation based on user criteria.

### 3. Property Automation via WhatsApp (`property automation wa`)
Automation for property business leads and re-engagement.
- **Features:**
    - `property_reactivation.json`: Re-engages old leads or contacts via WhatsApp (likely integrating with WAHA or similar services).

## 🚀 Usage

1. **Import Workflows:**
   - Import the `.json` files into your self-hosted n8n instance or n8n cloud.

2. **Configure Credentials:**
   - **Important:** All credential keys have been removed from these files for security.
   - You must re-connect your specific nodes (Telegram, Discord, Google Sheets, WhatsApp API, etc.) with your own credentials in n8n.

3. **Verify Settings:**
   - Check node parameters (like Channel IDs, Sheet IDs, API URLs) to ensure they match your environment.

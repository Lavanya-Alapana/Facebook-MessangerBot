# Facebook Messenger Bot Proof-of-Concept

This is a simple Node.js Express app that demonstrates how to create a Facebook Messenger bot using Meta’s Graph API and webhooks.

---

## Project Overview

You will:

- Create a Meta Business Developer App with Messenger + Webhooks
- Attach a Facebook Page you control
- Get Page Access Token, App ID, App Secret
- Use Graph API Explorer to test token and permissions
- Build two simple API endpoints:
  - `GET /webhook` for webhook verification
  - `POST /webhook` to receive and log messages
  - `POST /send` to send a "Hello from my bot!" message to a hardcoded user (PSID)
- Use ngrok to expose your local server over HTTPS
- Connect the webhook URL in Facebook Developer Portal
- Test the entire flow from your personal Facebook account to Page to bot reply

---

## Prerequisites

- Node.js installed
- Facebook Developer account and a Facebook Page you control
- ngrok installed

---

## Step 1: Create Facebook Developer App

1. Go to [Facebook Developer Portal](https://developers.facebook.com/apps/)
2. Create a new App of type **Business**
3. Add **Messenger** product
4. Connect a Facebook Page you manage
5. Get your **Page Access Token** under Messenger settings
6. Note your **App ID** and **App Secret**

---

## Step 2: Setup Environment Variables

Create a `.env` file in your project root:

```bash
PAGE_ACCESS_TOKEN=your_page_access_token_here
VERIFY_TOKEN=your_custom_verify_token_here
PORT=3000

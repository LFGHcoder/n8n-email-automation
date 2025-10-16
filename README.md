# Email Automation Workflow (n8n + Gmail + OpenAI)

This is a small workflow I built in **n8n** to automate email replies and keep a simple activity log.  
It connects **Gmail**, **OpenAI**, and **Google Sheets** to reply politely to new messages and record who contacted me and when.

---

## Overview

The idea behind this project was to make communication faster and more consistent.  
Instead of manually checking and replying to every email, this setup listens for new ones, filters out system messages, generates a short acknowledgment using AI, replies automatically, and logs the details to Google Sheets for reference.

---

## How It Works

1. **Gmail Trigger** – Watches a specific Gmail label for new messages.  
   I set filters so it ignores messages from “noreply,” “auto reply,” or “verification” emails.

2. **Prep Body (Function)** – Extracts useful fields like sender, subject, body text, and message/thread IDs.

3. **Guard Filter (Function)** – A simple code block that skips common automated emails (for example, “Out of Office” or “Password Reset”).

4. **OpenAI Chat Model** – Uses a lightweight model (`gpt-4.1-mini`) to create a short, professional acknowledgment message.

5. **Compose Reply & Gmail Node** – Sends the response directly to the sender, keeping it in the same email thread.

6. **Google Sheets Log** – Adds a new row with the timestamp, sender, and subject so I can track who got an automatic reply.

---

## Why I Built It

I wanted to explore how **automation + AI** can reduce repetitive work while keeping communication personal and professional.  
This setup could easily be adapted for small teams or startups that handle inquiries daily.

---

## Security & Privacy

- All credentials (Gmail, OpenAI, Google Sheets) are stored privately in my n8n instance.  
- The public version on GitHub only includes placeholders like `REPLACE_WITH_YOUR_OPENAI_CRED_ID`.  
- The workflow runs locally on my system, so no external data is exposed.  
- Only sender, subject, and timestamps are logged — not full message contents.

---

## How To Try It

1. Import `workflow_clean.json` into your n8n workspace.  
2. Connect your own Gmail, OpenAI, and Google Sheets credentials.  
3. Replace placeholder IDs with your own.  
4. Adjust the Gmail trigger query or label to control which emails get processed.  
5. Activate the workflow and test it by sending a message to yourself.

---

## Key Highlights

| Feature | Description |
|----------|-------------|
| Simple filters | Skips auto-replies and system messages. |
| Thread-safe | Replies in the same Gmail conversation. |
| Clean logic | Uses readable JavaScript instead of complex regex. |
| AI-written replies | Short, polite, and professional. |
| Logging | Keeps a record of each reply in Google Sheets. |

---



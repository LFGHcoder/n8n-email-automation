# Email Automation Agent (n8n Workflow)

This project automates email responses and logging using **n8n**, integrating Gmail, OpenAI, and Google Sheets.

## 🧠 Overview
The workflow listens for incoming emails via a Gmail Trigger, uses an AI model to generate a short, professional acknowledgment, replies automatically, and logs message details to Google Sheets.

It demonstrates lightweight automation suitable for small businesses or educational organizations with limited API infrastructure.

## ⚙️ Architecture
1. **Gmail Trigger** – Monitors specific labels for new messages.
2. **AI Agent + OpenAI Chat Model** – Summarizes message context and drafts a short, polite reply.
3. **Gmail Reply Node** – Sends the AI-generated response directly to the sender.
4. **(Optional) Google Sheets Node** – Logs sender, subject, and timestamp for review.

## 🧰 Technologies Used
- n8n (self-hosted, local instance)
- Gmail API
- OpenAI API
- Google Sheets API

## 🔒 Security Notes
This version uses placeholders for credentials and Spreadsheet IDs.  
All testing was done on my local n8n instance to ensure data privacy and compliance with Gmail’s automation limits.

## 🚀 How to Run
1. Import `workflow.json` into your n8n instance.
2. Connect your own Gmail, OpenAI, and Google credentials.
3. Adjust filters or labels in the Gmail Trigger as needed.
4. Activate the workflow to run automatically.

## 👨‍💻 About
Developed by **Lakshya Pandey**  
BSc Computer Science & Business Economics | Data & Tech Intern Candidate  
Contact: [your email] | [LinkedIn profile]

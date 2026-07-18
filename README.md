# Form to Email Automation

## 📌 Overview
This project is a workflow automation system built using **n8n** as part of Week 1 of the Abdanix Solutions internship. It automates the process of capturing form submissions and triggering multiple actions in response — without writing any backend code.

When a user submits a form, the workflow automatically:
- Sends a notification email to the admin
- Sends an auto-reply confirmation email to the submitter
- Logs the submission data into a Google Sheet
- Posts a real-time alert to a Discord channel

## 🛠️ Tools Used
- **n8n** – Workflow automation platform
- **Gmail SMTP** – For sending emails
- **Google Sheets API** – For data logging
- **Discord Webhooks** – For real-time notifications

## ⚙️ Workflow Structure
### Node Breakdown
| Node | Purpose |
|---|---|
| **On Form Submission** | Trigger node — captures Name, Email, and Message from the form |
| **Send Email (Notify)** | Sends the submitted details to the admin's inbox |
| **Auto Reply Email** | Sends a thank-you/confirmation message back to the submitter |
| **Log to Sheet** | Appends the submission as a new row in a Google Sheet |
| **Discord Notify** | Posts a formatted alert message to a Discord channel via webhook |

## 🧪 Testing
The workflow was tested by submitting sample data through the generated form URL and verifying that:
- The notification email was received correctly
- The auto-reply email was sent to the submitter
- A new row was added to the Google Sheet
- The Discord channel received the alert message

## 📂 Files in this Repository
- `workflow.json` — Exported n8n workflow (can be imported directly into n8n)

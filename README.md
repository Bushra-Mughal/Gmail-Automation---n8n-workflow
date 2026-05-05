# AI Gmail Automation (n8n)
This project automates personalized B2B cold email outreach using n8n, Google Sheets, and Gemini. It filters for pending leads, generates context-aware email content using AI, sends them via Gmail, and logs the results back to the spreadsheet.
# Workflow Overview
The workflow follows a sequential logic to ensure data integrity and personalized communication: 

- **Time Trigger:** Time execution to initiate the outreach process.

- **Data Retrieval:** Fetches rows from Google Sheets where Status is set to 'Not Sent'.  

- **AI Generation:** A Gemini Flash (AI Agent) node processes the Name, Company, and Purpose to craft a personalized subject line and email body.
- **Documents Retrieval:** Downloads document from Google Drive to send as an attachment with the email.

- **Email Dispatch:** Sends the generated content to the recipient's address using the Gmail node.  

- **Status Update:** Marks the record as Sent to prevent duplicate emails.
# Tech Stack
- n8n: Workflow automation and orchestration.

- Gemini (Flash 2.5): Generative AI for personalized emails.

- Google Sheets: Database for lead management and tracking.

- Gmail: SMTP/API provider for email delivery.

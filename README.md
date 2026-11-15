# 📧 AI Email Generator – n8n Automation

An AI-powered email automation workflow built using **n8n, OpenAI, Google Sheets, and Gmail**.

This project generates personalized professional emails based on user inputs, formats the generated content into HTML, stores the email details in Google Sheets, and automatically sends the email through Gmail.

## 🚀 Workflow Overview

The workflow automates the complete email generation and delivery process.

1. **Form Submission:** Collects sender name, recipient name, recipient email, email purpose, preferred tone, and additional notes.
2. **AI Email Generation:** Uses an OpenAI-powered AI Agent with GPT-4o-mini to generate a personalized subject line and email content.
3. **HTML Formatting:** A JavaScript node converts the generated email into a structured HTML layout.
4. **Google Sheets Integration:** Stores the generated subject and email output in Google Sheets.
5. **Gmail Integration:** Automatically sends the formatted email to the specified recipient.

## ✨ Features

- AI-generated personalized emails.
- Multiple email purposes, including job applications, internship applications, leave requests, business inquiries, and personal messages.
- Multiple writing tones: Professional, Formal, Friendly, Polite, and Casual.
- Additional notes for customized email generation.
- Automatically generated subject lines.
- HTML-formatted email output.
- Google Sheets integration for email record storage.
- Automatic Gmail delivery.

## 🧰 Technology Stack

| Technology | Purpose |
|---|---|
| n8n | Workflow automation |
| OpenAI GPT-4o-mini | AI email generation |
| JavaScript | Email formatting |
| Google Sheets | Data storage |
| Gmail API / OAuth2 | Email delivery |

## 🔄 Workflow Architecture

```text
Form Submission
      |
      v
   AI Agent
      |
 OpenAI Model
      |
      v
JavaScript Formatter
      |
      v
 Google Sheets
      |
      v
    Gmail
      |
      v
 Email Delivered
```

## ⚙️ Setup Instructions

### Prerequisites

- An n8n account or self-hosted n8n instance.
- OpenAI API access and credentials.
- A Google account with Google Sheets access.
- Gmail OAuth2 credentials configured in n8n.

### 1. Clone the Repository

```bash
git clone https://github.com/romilpatel740-hue/Email_Generator_Workflow.git
```

### 2. Import the Workflow

1. Open your n8n instance.
2. Select the workflow menu.
3. Choose **Import from File**.
4. Select `Email_Generator.json`.

### 3. Configure OpenAI

1. Open the OpenAI Chat Model node.
2. Add your OpenAI API credentials.
3. Select GPT-4o-mini or another supported model.

### 4. Configure Google Sheets

1. Create a Google Sheet for storing generated emails.
2. Add columns named `Subject` and `Email`.
3. Open the Append row in sheet node.
4. Connect your Google Sheets credentials.
5. Replace `YOUR_GOOGLE_SHEET_ID` with your actual spreadsheet ID.

### 5. Configure Gmail

1. Open the Send a message node.
2. Connect your Gmail OAuth2 credentials.
3. Verify the recipient email, subject, and HTML message mappings.

### 6. Test and Activate

1. Save the workflow.
2. Test it using your own email address first.
3. Verify that the generated email is stored in Google Sheets and delivered correctly.
4. Activate or publish the workflow when everything works.

**Important:** Submitting the form triggers automatic email delivery. Test carefully before sharing the production form link.

## 📸 Workflow Preview

The workflow screenshot is available below:

<img width="1010" height="379" alt="AI Email Generator n8n Workflow" src="https://github.com/user-attachments/assets/70e4f463-e6bd-4afe-adbd-3910780e92fd" />

## 🔐 Security Notes

- Never upload API keys, OAuth tokens, or credentials to GitHub.
- Configure credentials securely inside n8n.
- Use your own test email address when testing automated delivery.
- Avoid exposing sensitive recipient information in publicly accessible spreadsheets.

## 👨‍💻 Developer

**Romil Patel**

- GitHub: [romilpatel740-hue](https://github.com/romilpatel740-hue)
- LinkedIn: [Romil Patel](https://www.linkedin.com/in/romil-patel-100263320/)

---

⭐ Feel free to explore the workflow and adapt it to your own email automation needs.

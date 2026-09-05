# 📧 AI Email Generator (n8n Workflow)

An automated n8n workflow that generates personalized, professional emails using OpenAI, stores the records in Google Sheets, and sends the final email directly through Gmail.

---

## 🚀 Workflow Overview

1. **Form Trigger (`On form submission`):** Captures user inputs including sender/recipient names, email addresses, purpose (e.g., Job Application, Leave Request), tone, and additional notes.
2. **AI Agent & Language Model (`OpenAI Chat Model`):** Uses structured prompts to draft a well-formatted email and matching subject line in valid JSON format.
3. **HTML Formatter (`Code in JavaScript`):** Formats the generated email into a clean HTML layout with inline CSS styling.
4. **Data Logging (`Append row in sheet`):** Saves the email details and subject line into a designated Google Sheet.
5. **Email Delivery (`Send a message`):** Sends the formatted HTML email directly to the recipient via Gmail.

---

## 🛠️ Setup Instructions

### 1. Import the Workflow
1. Download the `Email_Generator.json` file from this repository.
2. Open your [n8n canvas](https://n8n.io/).
3. Click the **`...` (menu)** in the top right corner and select **Import from File**.
4. Upload `Email_Generator.json`.

### 2. Configure Credentials & Placeholders
* **OpenAI:** Connect your OpenAI API credentials in the `OpenAI Chat Model` node and select your preferred model (e.g., `gpt-4o-mini`).
* **Google Sheets:** Open the `Append row in sheet` node, select your Google Sheets credentials, and replace `YOUR_GOOGLE_SHEET_ID` with your actual Google Sheet ID.
* **Gmail:** Connect your Gmail OAuth2 credentials in the `Send a message` node.

### 3. Activate
1. Publish/Activate the workflow in n8n.
2. Open the **Form Trigger** node to copy your production form link and test it out!

### 4. Workflow Preview
<img width="1010" height="379" alt="Screenshot (149)" src="https://github.com/user-attachments/assets/70e4f463-e6bd-4afe-adbd-3910780e92fd" />


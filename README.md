# Bulk Email Dispatcher with AI Agent & n8n

An automated workflow built in **n8n** that integrates an **AI Agent** (powered by OpenAI / Custom Chat Model) with **Google Sheets** and **Gmail** to dynamically generate and send personalized email content in batches.

---

## 🚀 Features
- **Dynamic AI Content Generation:** Uses a strictly-prompted AI Agent to generate clean, professional email bodies.
- **Batch Processing:** Utilizes n8n's `Loop Over Items` node to safely handle lists of email recipients from Google Sheets.
- **Strict Guardrails:** System prompts ensure no tool names (like Gmail or Google Sheets) or placeholders leak into the final output.

---

## 📂 Workflow Architecture
1. **Google Sheets Trigger / Read Node:** Fetches recipient email addresses.
2. **Loop Over Items:** Iterates through the spreadsheet rows one by one.
3. **AI Agent + OpenAI Chat Model:** Generates the email text based on predefined system constraints.
4. **Gmail Node:** Dispatches the generated email to the current recipient.

---

## 🛠️ Prerequisites & Setup
1. Import `n8n-ai-bulk-email-workflow.json` into your n8n instance.
2. Set up your Google Sheets credentials and prepare a sheet with an `email` column.
3. Configure your OpenAI / Chat Model credentials (or compatible API base URL).
4. Connect your Gmail account credential to the Gmail node.
5. Execute and enjoy automation!

# 📩 Add new incoming emails to a Google Sheets spreadsheet as a new row

## 📝 Overview  
This n8n workflow automates the process of capturing and storing incoming email details in a structured spreadsheet format, such as Google Sheets or Excel. Whenever a new email is received, the workflow extracts key details—including the sender’s email, subject, email body, and optional attachments—and logs them as a new row in the spreadsheet.

You can customise this workflow to extract additional details, filter emails based on specific criteria, or send notifications when new entries are added.

### 🔹 Key Features:  
✅ **Automatically triggers** when a new email arrives.  
✅ **Extracts sender email, subject, body, and attachments**.  
✅ **Logs email details** as a new row in Google Sheets.  
✅ **Customizable filters** to capture specific emails.  

This workflow is useful for **automated email tracking, reporting, and structured storage**.  

---

## ✅ Prerequisites  

Before setting up this workflow, ensure:  

 **Email Provider Access**  
   - You have access to **Gmail, Outlook, or an IMAP-supported email service**.  

**n8n Gmail Node**  
   - The **Gmail Node** is enabled in **n8n**.  

**Google OAuth2 Authentication**  
   - n8n is authenticated with **Google OAuth2** to access your inbox.  

**Gmail API Enabled**  
   - Ensure the **Gmail API** is enabled in **Google Cloud Console**.  

**Google Sheets Setup**  
   - You have an existing **Google Sheet** where data will be stored.  
   - The **Google Sheets API** is enabled.  
   - n8n is authenticated with **Google OAuth2** for Google Sheets access.  

---

## 🔄 Workflow Steps  

### **Step 1: Add the Gmail Trigger Node**
📌 **Action**: Detects new emails in Gmail.  

- Click on **"Add Node"** and search for **"Gmail"**.  
- Select **"Gmail Trigger"** and add it.  
- Under **Authentication**, click **"Create New"** and authenticate with Google.  
- In the **Trigger Event** field, select **"Message Received"**.  
- (Optional) Add filters:  
  - **Label/Mailbox**: Listen to emails from a specific folder.  
  - **From Address**: Filter emails by sender.  
- Click **"Execute Node"** to test.  
- Click **"Save"**.  

---

### **Step 2: Store Email Data in Google Sheets**
📌 **Action**: Logs extracted email details into Google Sheets.  

- Click on **"Add Node"** and search for **"Google Sheets"**.  
- Authenticate using your **Google OAuth2 credentials**.  
- Select the target **Spreadsheet and Sheet Name**.  
- Set **Operation** to **"Append Row"**.  
- Map extracted email fields to the correct columns:  
  - 📧 **Sender Email**  
  - 📝 **Subject**  
  - 📄 **Email Body**  
  - 📎 **Attachments (if any)**  
- Click **"Execute Node"** to test.  
- Click **"Save"**.  

---

### **Final Step: Connect and Run the Workflow**
✅ **Attach both nodes**:  
   - **Gmail Trigger** → **Google Sheets (Append Row)**  

✅ **Run the workflow manually**.  
✅ **Send a test email to verify**.  
✅ **Check Google Sheets for the logged email data**.  

---

## 📌 Outcome  

Once set up, this workflow will:  
✅ **Automatically capture incoming emails** in real time.  
✅ **Log essential email details** into a structured spreadsheet.  
✅ **Provide an organized and searchable email log**.  

---

## 🚀 About WeblineIndia  

This workflow is built by the **AI development team at WeblineIndia**.  

📌 **Who are we?**  
✔ **25+ years** of software development experience.  
✔ **3,500+ successful projects** delivered across **25+ countries**.  
✔ Expertise in **no-code automation, AI systems, and enterprise solutions**.  

📩 **Need a custom workflow?** Hire our AI developers to build **tailored automation solutions** for your business!  

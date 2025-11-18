## Daily Social Media Post Automation (n8n Workflow)

This repository contains an **n8n workflow** that automates daily social media posting from Google Sheets.  
It fetches pending posts, generates AI-written captions and images, and publishes them to Facebook.

---

## 🚀 Features
- **Daily Trigger**: Runs every day at 9 AM.
- **Google Sheets Integration**: Fetches rows marked as `Pending`.
- **AI Caption Generation**: Uses OpenAI to create short, catchy posts.
- **Image Generation**: Creates images based on prompts in the sheet.
- **Facebook Posting**: Publishes the generated content to Facebook.
- **Status Update**: Marks the row as `Posted` after successful publishing.

---

## 📂 Workflow Structure
1. **Daily Trigger** → Starts the workflow.
2. **Fetch Unposted Row** → Reads the next pending post from Google Sheets.
3. **Message a model** → Generates a caption using OpenAI.
4. **Generate Image** → Creates an image from the prompt.
5. **Post to Facebook** → Publishes the caption + image.
6. **Mark as Posted** → Updates the sheet status.

---

## 🔧 Setup Instructions
1. Import the workflow JSON into your **n8n instance**.
2. Configure the following credentials in n8n:
   - **Google Sheets OAuth2 API**
   - **OpenAI API**
   - **Facebook Graph API**
3. Update the **spreadsheetId

# AI Email Triage Agent 🤖📬
A Python-based AI agent that monitors your Gmail inbox, categorizes emails using Azure OpenAI, and sends high-priority "Action" items directly to your WhatsApp.

## 🚀 Features
Smart Categorization: Uses GPT-4 to distinguish between tasks, ads, and general updates.

Instant Notifications: Delivers a concise to-do list via WhatsApp (Twilio API).

Privacy Focused: Runs locally or as a background service.

Secure Auth: Implements Google OAuth 2.0 with token refreshing to avoid repeated browser logins.

## 🛠️ How It Works
Fetch: The script queries the Gmail API for messages received in the last 24 hours.

Analyze: Email snippets are sent to Azure OpenAI with a custom prompt to determine intent.

Notify: If an email requires action, a formatted WhatsApp message is sent via Twilio.

Schedule: The agent uses the schedule library to run automatically at a set time every day.

## 📦 Setup & Installation
Clone the repo:

Bash
git clone https://github.com/your-username/ai-email-triage-agent.git
cd ai-email-triage-agent
Install dependencies:

Bash
pip install -r requirements.txt
API Setup:

Obtain a credentials.json from the Google Cloud Console.

Get your Azure OpenAI endpoint and key from the Azure Portal.

Sign up for a Twilio Sandbox to get your WhatsApp SID and Token.

Environment Variables:

Create a .env file (or hardcode your keys locally—never commit them!)

Run the Agent:

Bash
python email_agent.py
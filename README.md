# 🛡️ AI-Driven Security Alert Analysis & Executive Briefing

## 📌 Overview

This project is an **AI-powered n8n workflow** that turns raw security events from tools such as **Wazuh**, SIEM platforms, or other compatible sources into a clear executive security briefing.

The workflow helps security teams reduce alert fatigue by filtering noisy logs, identifying important alerts, and generating a business-friendly summary that can be copied, reviewed, or used in reporting.

---

## ✨ Features

- ⚡ Automated daily security event analysis
- 🤖 AI-powered alert filtering
- 📦 Structured JSON alert extraction
- 📊 Executive-level security summary generation
- 💼 Business impact explanation
- 🚨 Key threat pattern identification
- 📝 Markdown-to-HTML report formatting
- 🧠 Two-stage AI processing for better accuracy
- 🔧 Customizable prompts and workflow logic
- 🛡️ Designed for Wazuh, SIEM, and security event data sources

---

## 🏗️ Workflow Architecture

<img width="801" height="438" alt="image" src="https://github.com/user-attachments/assets/e7bee152-bac2-4aec-81d3-1a06a678bc92" />

---

## ⚙️ How It Works

### ⏰ 1. Scheduled Execution

The workflow runs automatically every day at **8 AM**.

### 🔑 2. Initial Prompt Setup

The workflow sets the API key and prepares the initial AI prompt for security event analysis.

### 📥 3. Daily Security Event Retrieval

The workflow calls the connected security event source and retrieves daily security events in JSON format.

### 🧹 4. Alert Parsing

The returned alert data is parsed into a structured alert array.

### ✅ 5. Conditional Check

The workflow checks whether important or relevant alerts exist.

- ❌ If no significant alerts are found, the workflow stops.
- ✅ If alerts are found, the workflow continues to the summary generation stage.

### 🧠 6. Executive Summary Prompt

A second prompt is prepared to convert technical alert data into a business-friendly executive summary.

### 📊 7. Executive Summary Generation

The AI generates a concise security briefing focused on:

- 🚨 Important alerts
- 💼 Business impact
- 📈 Key threat patterns
- ⚠️ Risk explanation
- 🛠️ Recommended action

### 📝 8. Final Briefing Formatting

The generated briefing is prepared as final Markdown content.

### 🌐 9. Markdown to HTML Conversion

The final Markdown briefing is converted into HTML format for easier viewing, sharing, or future integration with email, dashboards, or reporting tools.

---

## 🧠 Two-Stage AI Processing

### 🔍 Stage 1: Intelligent Filtering and Data Structuring

The first AI stage reviews raw security events and converts them into a clean, structured JSON array. This helps remove low-value noise and keeps only the alerts that matter.

### 👨‍💼 Stage 2: Executive Summarization

The second AI stage acts like a Senior Security Analyst. It converts the structured alert data into a simple, executive-friendly summary that non-technical stakeholders can understand.

---

## 🧩 Workflow Nodes

| 🧱 Node | 🎯 Purpose |
|---|---|
| ⏰ Run Daily at 8 AM | Starts the workflow on a daily schedule |
| 🔑 Set API Key & Initial Prompt | Sets credentials and the first AI prompt |
| 📥 Get Daily Events as JSON | Retrieves daily security events |
| 🧹 Parse Alert Array | Converts returned data into a usable alert array |
| ✅ If | Checks whether alerts exist |
| 🧠 Set Prompt for Summary | Prepares the executive summary prompt |
| 📊 Generate Executive Summary | Generates the business-friendly security summary |
| 📝 Set Final Briefing | Stores the final briefing content |
| 🌐 Convert Markdown to HTML | Converts the briefing into HTML format |

---

## 📄 Example Output

```text
Daily Security Executive Briefing

Summary:
Several failed login attempts were detected from external IP addresses. One endpoint also showed suspicious command execution activity.

Business Impact:
These events may indicate attempted unauthorized access or early-stage compromise activity.

Risk Level:
Medium

Recommendation:
Review affected user accounts, validate endpoint activity, and confirm that MFA is enabled for all privileged users.
```

---

## 🎯 Benefits

### 👨‍💻 For Security Teams

- ⏳ Saves time on manual report writing
- 🔕 Reduces alert fatigue
- 🎯 Helps prioritize important security events
- 📋 Improves consistency in daily reporting

### 🏢 For Leadership

- 📢 Clear and simple security updates
- 📈 Better understanding of business risk
- ✅ Actionable recommendations without technical complexity

---

## 🛠️ Technologies Used

- ⚡ n8n
- 🤖 AI / LLM workflow automation
- 🛡️ NixGuard Security RAG Connector
- 🚨 Wazuh or SIEM event data
- 📦 JSON processing
- 📝 Markdown formatting
- 🌐 HTML conversion

---

## 💡 Use Cases

- 📅 Daily security briefings
- 🛡️ SOC alert summarization
- 📊 SIEM log reporting
- 👔 Executive cybersecurity updates
- 🏢 Internal security posture reviews
- 🚨 Incident summary preparation

---

## 🚀 Setup Instructions

1. 📥 Import the workflow JSON file into n8n.
2. 🔗 Configure the NixGuard Security RAG connector.
3. 🔑 Add your required API key or credentials.
4. 🛡️ Connect your Wazuh, SIEM, or security event source.
5. ⚙️ Adjust the initial prompt based on your alert format.
6. 🧠 Customize the executive summary prompt if needed.
7. 🧪 Run the workflow manually for testing.
8. ✅ Activate the daily schedule.

---

## 🔧 Customization Ideas

You can extend this workflow by adding:

- 📧 Email delivery
- 💬 Slack or Microsoft Teams notifications
- 📄 PDF report generation
- 🎫 Incident ticket creation
- 📊 Dashboard storage
- 📈 Risk scoring logic
- 🌐 Multi-SIEM support

---

## 👥 Who Is This For?

- 🛡️ Security Analysts
- 🚨 SOC Teams
- ⚙️ SecOps Engineers
- 🔧 DevOps Teams
- 👨‍💼 IT Managers
- 🧑‍💻 Security Consultants
- 📢 Anyone who needs to convert security alerts into business-friendly reports

---

## 🔮 Future Improvements

- 📧 Add email delivery node
- 💬 Add Slack or Teams integration
- 📄 Add automatic PDF export
- 📈 Add severity-based risk scoring
- 🎫 Add incident ticket creation
- 📊 Add weekly and monthly trend summaries

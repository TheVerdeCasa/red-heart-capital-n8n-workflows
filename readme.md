# Red Heart Capital - n8n Automation Workflows

Complete automation system for Red Heart Capital loan operations using n8n, Pipedrive, Slack, and Google Sheets.

## 📋 Workflows

| # | Name | Status | Description |
|---|------|--------|-------------|
| 01 | [Sheets to Pipedrive](workflows/01-sheets-to-pipedrive.json) | ✅ Active | Syncs Facebook leads from Google Sheets to Pipedrive |
| 02 | Incoming Email Handler | 🔄 In Progress | Routes emails to Slack channels per deal |
| 03 | Document Processor | 📝 Planned | Processes uploaded documents via Couchdrop |
| 04 | Post-Call Deliverable | 📝 Planned | Generates PDF after JustCall recordings |
| 05 | Email Reminders | 📝 Planned | Smart email follow-up system |

## 🔧 Tech Stack

- **n8n**: Workflow automation
- **Pipedrive**: CRM and deal management
- **Slack**: Team notifications and collaboration
- **Google Sheets**: Lead capture from Facebook
- **Couchdrop**: Secure document collection (planned)
- **JustCall**: Call recording and transcription (planned)

## 📥 How to Import Workflows

### Method 1: Direct URL Import (Recommended)
1. Click on any workflow file above
2. Click the "Raw" button
3. Copy the URL
4. In n8n: Click ⋯ menu → "Import from URL"
5. Paste the raw URL
6. Click "Import"

### Method 2: Manual Copy/Paste
1. Click on the workflow file
2. Click "Copy raw file" button
3. In n8n: Click ⋯ menu → "Import from File"
4. Paste the JSON
5. Click "Import"

## ⚙️ Setup Requirements

### Required Credentials in n8n:
- Google Sheets OAuth2 API
- Pipedrive API (get from Settings → Personal → API)
- Slack API

### Required Pipedrive Custom Fields:
```
First Name (text)
Last Name (text)
Email (text)
Phone (text)
Reason for Capital (text)
Amount Needed (text)
Property Type (text)
Property Location (text)
Stage of Deal (text)
Completed Projects (text)
Deal Liquidity (text)
Fico Range (text)
```

## 📊 Google Sheet Structure

Your Facebook lead form should populate these columns:

| Column | Field Name | Type |
|--------|------------|------|
| A | First Name | Text |
| B | Last Name | Text |
| C | Email | Email |
| D | Phone | Phone |
| E | Reason for Capital | Dropdown |
| F | Amount Needed | Dropdown |
| G | Property Type | Dropdown |
| H | Property Location | Text |
| I | Stage of Deal | Dropdown |
| J | Completed Projects | Dropdown |
| K | Deal Liquidity | Dropdown |
| L | Fico Range | Dropdown |

## 🔐 Security Notes

- ⚠️ Never commit actual API keys or credentials to this repository
- ✅ Use n8n's credential management system
- ✅ Keep this repository private
- ✅ Only share workflow JSON files, never credentials

## 📝 Documentation

- [Setup Guide](docs/setup-guide.md) - Complete setup instructions
- [Field Mappings](docs/field-mappings.md) - How data maps between systems
- [Troubleshooting](docs/troubleshooting.md) - Common issues and solutions

## 🆘 Support

For issues or questions:
1. Check the [Troubleshooting Guide](docs/troubleshooting.md)
2. Review n8n execution logs
3. Contact your automation consultant

## 📅 Last Updated

February 15, 2026

---

**Built with ❤️ for Red Heart Capital**
```

Click "Commit new file"

---

### **FILE 2: workflows/01-sheets-to-pipedrive.json**

**1. Create the workflows folder:**
```
Click "Add file" → "Create new file"
Filename: workflows/01-sheets-to-pipedrive.json

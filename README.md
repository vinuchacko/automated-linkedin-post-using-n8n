# Automated LinkedIn Post Pipeline using n8n & Gemini

An automated, hands-off content publishing pipeline that bridges AI content generation with automated social scheduling. 

### How It Works

1. **AI Generation:** A scheduled job using **Gemini Spark** automatically drafts relevant, structured LinkedIn posts.
2. **Content Queue:** The generated posts, topics, and metadata are saved to a **Google Sheet** marked with a pending status.
3. **Orchestration via n8n:** An **n8n** workflow periodically queries the sheet for unpublished records.
4. **Publishing & Sync:** n8n posts the selected update directly to **LinkedIn** via the official API and marks the spreadsheet row as `Published` upon success.

### Tech Stack

* **Workflow Automation:** n8n
* **AI Model:** Google Gemini (Gemini Spark)
* **Data Store / Content Calendar:** Google Sheets
* **Destination:** LinkedIn API (OAuth 2.0 / OpenID Connect)

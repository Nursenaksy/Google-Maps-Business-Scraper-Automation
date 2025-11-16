# Google-Maps-Business-Scraper-Automation
This project is an automation system that searches for businesses on Google Maps based on your criteria and automatically saves the collected business information into Google Sheets. The system uses an OpenAI Agent, Google Maps Search Tool, and Google Sheets integration. 
🚀 Features

Automatically searches for businesses on Google Maps using keywords and location.

Collects business details such as:

Name

Address

Phone number

Rating

Status (open/closed)

Additional available information

Saves the collected data directly into Google Sheets.

Entire workflow is managed by an AI Agent.

Uses 2 independent workflows:

1st Workflow: Fetches business data from Google Maps.

2nd Workflow: Appends the data to Google Sheets.

🧠 System Architecture
Workflow 1: AI Agent Business Finder

Triggered by a chat message. The AI Agent performs a Google Maps search using the GoogleMaps2 tool, processes the business data, and triggers the second workflow with the extracted information.
File: workflow-agent.json

Workflow 2: Sheets Appender

Triggered by Workflow 1. Receives the processed business information and appends it as a new row in Google Sheets.
File: workflow-sheets.json
📂 Project Structure
workflow-agent.json        # Workflow that searches Google Maps
workflow-sheets.json       # Workflow that writes data to Google Sheets
README.md                  # Project documentation

🔧 Requirements

OpenAI API access

Google Maps Search API (GoogleMaps2 Tool)

Google Sheets API

Automation platform with multi-workflow support (OpenAI Automations)

⚙️ Setup Instructions

Upload both workflow files:

workflow-agent.json

workflow-sheets.json

Connect your Google Sheets account and select your target sheet.

Add your Google Maps API key.

Configure the GoogleMaps2 tool inside the AI Agent.

Ensure Workflow 1 successfully triggers Workflow 2 with the correct data payload.

▶️ Usage

Run the automation by sending a command such as:

Find coffee shops in New York City


The AI Agent will search Google Maps, extract business information, and automatically append the results to your connected Google Sheet. The sheet grows dynamically as more queries are executed.
🤝 Contribution

Contributions and pull requests are welcome. Feel free to improve or extend the project.

📜 License

This project is released under the MIT License.




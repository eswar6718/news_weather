📊 AI News Chatbot Workflow (n8n)
🚀 Overview

This project is an AI-powered chatbot workflow built using n8n that integrates with Telegram to provide real-time news and current event responses.

The system ensures 100% factual responses by relying only on data fetched from an MCP (Model Context Protocol) server, avoiding hallucinations or assumptions.

⚙️ Features
🤖 AI chatbot integrated with Telegram
🧠 Context-aware conversations using memory buffer
🌐 Real-time data fetching via MCP server
🔍 Web search support using SerpAPI
🌦️ Weather API integration (Tomorrow.io)
📧 Gmail integration for sending emails
❌ Strict filtering: Only answers news/current events
🎭 Creative refusal for unrelated queries
🏗️ Workflow Architecture
Telegram Trigger
Receives user messages
AI Agent
Processes user input
Uses Groq LLM for responses
Maintains memory context
MCP Client
Fetches real-time verified data
External Tools
SerpAPI → search data
HTTP API → weather data
Gmail → send emails
Response Output
Sends reply back to Telegram user
🔒 System Behavior Rules
Only responds to news & current events
No answers from memory or assumptions
Must rely on MCP server data
If data is unavailable → clearly states it
Non-relevant queries → creative refusal message
🛠️ Tech Stack
n8n
Telegram Bot API
Groq LLM
MCP Server (custom endpoint)
SerpAPI
Tomorrow.io Weather API
Gmail API
🔧 Setup Instructions
1. Clone / Import Workflow
Import the provided JSON file into n8n
2. Configure Credentials
Telegram Bot API
Groq API Key
SerpAPI Key
Gmail OAuth
Tomorrow.io API Key
3. Set MCP Endpoint

Update the MCP client URL:

https://<your-n8n-instance>/mcp/<endpoint-id>
4. Activate Workflow
Enable the workflow in n8n
Test using Telegram bot
📌 Usage
Send a message via Telegram
Ask about current news/events
Get short, factual responses (2–3 lines)
⚠️ Limitations
Cannot answer general knowledge questions
Fully dependent on MCP server availability
Responses are intentionally short
📄 Workflow File

Included in this repository:
My workflow.json

👨‍💻 Author

Eswar Bongu

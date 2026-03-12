# 🤖 AI Business Morning Briefing System
Automated daily business briefing pipeline built for a manufacturing & engineering company.

## What It Does
Every morning at 7AM, this system automatically:
- Pulls live business data from Google Sheets
- Sends data to Groq AI for intelligent summarization
- Delivers a concise AI-written briefing directly to WhatsApp

No manual effort. Owner wakes up to a full business summary on WhatsApp.

## Tech Stack
- **n8n** — workflow automation & scheduling
- **Groq API** — AI summarization (LLM)
- **Twilio WhatsApp API** — message delivery
- **Google Sheets** — live data source

## Pipeline Flow
Google Sheets → n8n → Groq AI → WhatsApp

## Business Value
Replaces manual morning reporting. Saves ~1 hour daily.
Built as a proof-of-concept for a real business deployment.

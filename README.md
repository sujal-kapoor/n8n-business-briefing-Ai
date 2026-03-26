# 🤖 AI Business Morning Briefing System

**Live in production. Built solo. Zero manual steps.**

> Every morning at 6:30 AM, a business owner receives a WhatsApp message with AI-analysed KPIs, flagged anomalies, and prioritised action items — pulled automatically from live data. No dashboards to open. No spreadsheets to check. Just a message that tells you what matters.

---

## 📸 System at a Glance

```
Google Sheets API  →  Groq LLM (Llama 3)  →  Twilio WhatsApp
     (Data)               (Intelligence)           (Delivery)
         └──────────── n8n Orchestration ───────────┘
                    (Scheduling + Error Handling)
```

| Metric | Value |
|--------|-------|
| 🟢 Status | **Live — Active Daily** |
| 👤 Built by | Sujal Kapoor — solo, end to end |
| ⏱️ Delivery time | 6:30 AM daily, automated |
| 🔗 Services integrated | Google Sheets, Groq API, Twilio, n8n |
| 🧠 LLM | Llama 3 via Groq (sub-2s inference) |
| 📲 Output channel | WhatsApp Business API |

---

## 🧩 How It Works

### Step 1 — Data Ingestion
Google Sheets API pulls structured business KPIs (sales figures, inventory, daily targets) into the pipeline as a normalised JSON payload. No manual export needed.

### Step 2 — AI Processing
Groq LLM API (Llama 3) receives the structured data with a custom system prompt engineered for consistent, structured output. Performs:
- Anomaly detection (metrics outside target range)
- Trend analysis (day-over-day comparison)
- Priority ranking of action items
- Human-readable briefing generation

All in under 2 seconds.

### Step 3 — Delivery
Twilio WhatsApp Business API formats and delivers the briefing to the client's WhatsApp — rich text, structured sections, action items highlighted.

### Step 4 — Orchestration
n8n workflow engine manages:
- Daily scheduling (6:30 AM)
- Error handling + retry logic
- Logging
- Zero-downtime autonomous operation

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Workflow Orchestration | n8n |
| AI / LLM | Groq API (Llama 3) |
| Messaging | Twilio WhatsApp Business API |
| Data Source | Google Sheets API |
| Scripting | Python |
| Prompt Engineering | Custom system prompts |

---

## 💡 What I Built — End to End

- ✅ Identified the business problem and defined output requirements before touching any tool
- ✅ Designed full data flow architecture: ingestion → processing → formatting → delivery
- ✅ Built and tested each API integration independently, then composed into a single workflow
- ✅ Engineered LLM system prompt for consistent, structured output across variable input data
- ✅ Implemented scheduling, error handling, and retry logic for production reliability
- ✅ Iterated on output format based on real user feedback from the live client
- ✅ Documented full system architecture

---

## 📁 Repository Structure

```
ai-business-briefing-n8n/
├── workflow/
│   └── briefing_workflow.json     # n8n workflow export
├── scripts/
│   ├── data_fetch.py              # Google Sheets ingestion
│   ├── llm_processor.py           # Groq API + prompt engineering
│   └── whatsapp_delivery.py       # Twilio formatting + send
├── prompts/
│   └── briefing_system_prompt.txt # LLM system prompt
├── docs/
│   └── architecture.md            # System design notes
└── README.md
```

---

## 🔧 Setup

```bash
git clone https://github.com/sujal-kapoor/ai-business-briefing-n8n
cd ai-business-briefing-n8n
pip install -r requirements.txt
```

Set environment variables:
```bash
GROQ_API_KEY=your_key
TWILIO_ACCOUNT_SID=your_sid
TWILIO_AUTH_TOKEN=your_token
GOOGLE_SHEETS_CREDENTIALS=path/to/creds.json
```

Import `workflow/briefing_workflow.json` into your n8n instance and activate.

---

## 📬 Contact

**Sujal Kapoor**  
sujal.kapoor0418@gmail.com  
[LinkedIn](https://linkedin.com/in/sujal-kapoor) • [GitHub](https://github.com/sujal-kapoor)

---

*Built with obsessive attention to making something that actually works in production, not just in demos.*

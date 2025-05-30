Security Awareness Coach

Security Awareness Coach is an AI-powered workflow built with n8n and Claude (Anthropic API) to help teams and individuals stay sharp on cybersecurity, one question at a time.

It automatically turns current cybersecurity headlines into a plain-English summary and a multiple-choice awareness question, delivered directly to your inbox.

🚀 Features

📰 Fetches real-time cybersecurity news from BleepingComputer

🤖 Summarises and generates questions via Claude (Anthropic API)

📩 Sends a formatted email with summary + quiz question via Gmail

🔁 Can run on a schedule (daily/weekly)

💡 Why Use This

Traditional security awareness training is long, boring, and infrequent.

This workflow brings:

✍️ Bite-sized microlearning

🔐 Real-world context (based on actual breaches/fixes)

🧠 Knowledge reinforcement via daily quiz-style delivery

Perfect for:

Security teams

Developers

Anyone who wants to stay sharp without watching a 30-minute video

📦 How It Works

Trigger (manual or scheduled)

RSS Read: Pulls the latest article from BleepingComputer

Code Node: Selects top article and extracts title + snippet

HTTP Request: Sends article to Claude API with prompt

Code Node: Extracts Claude's response

Gmail Node: Sends a clean email with a summary + question

🛠 Setup Instructions

Prerequisites

n8n Cloud or self-hosted instance

Claude API key (from Anthropic)

Gmail account (OAuth2 connected in n8n)

1. Import Workflow

Download the security-awareness-coach.json file (included in this repo)

In n8n, click Import Workflow → paste or upload a file

2. Set Variables

In the HTTP Request node:

Add Header: x-api-key: your Claude API key

Add Header: anthropic-version: 2023-06-01

Content-Type: application/json

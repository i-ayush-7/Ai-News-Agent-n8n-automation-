# Ai-News-Agent-n8n-automation-

# 🤖 AI News Daily Digest Agent

> **Automated daily AI news briefings delivered straight to Telegram.**

[![n8n](https://img.shields.io/badge/Workflow-n8n-ff6e5c?style=flat&logo=n8n)](https://n8n.io/)
[![Node.js](https://img.shields.io/badge/Runtime-Node.js-339933?style=flat&logo=node.js)](https://nodejs.org/)
[![Gemini](https://img.shields.io/badge/AI-Google_Gemini-8E75B2?style=flat&logo=google)](https://deepmind.google/technologies/gemini/)
[![Telegram](https://img.shields.io/badge/Chat-Telegram-26A5E4?style=flat&logo=telegram)](https://telegram.org/)

## 📖 Overview

This project is an automated AI Agent designed to keep you updated with the latest developments in Artificial Intelligence without the noise.

Running on an **n8n** workflow server, the agent scrapes/fetches the latest headlines from **TechCrunch** every morning at **7:00 AM**. It then uses **Google's Gemini AI** to analyze, filter, and summarize the articles into a digestible format before sending a briefed report to a private **Telegram** chat.

## ✨ Key Features

## 🛠️ Tech Stack

* **Workflow Automation:** n8n
* **Scripting:** Node.js (used within n8n Function nodes for data parsing)
* **LLM Engine:** Google Gemini API
* **Notification Interface:** Telegram Bot API
* **Data Source:** TechCrunch (RSS/Scraping)

## 🚀 Getting Started

### Prerequisites

Before setting up the workflow, ensure you have the following:

1.  **n8n Instance:**
2.  **Google Gemini API Key:** Get your free API key from [Google AI Studio](https://aistudio.google.com/api-keys).
3.  **Telegram Bot:**

### Installation & Setup

#### 1. Clone or Download
Clone this repository to access the workflow JSON file.
```bash
git clone [https://github.com/yourusername/ai-news-agent.git](https://github.com/yourusername/ai-news-agent.git)

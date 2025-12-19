# 🤖 Ai News Agent

> **Automated daily AI news briefings delivered straight to Telegram.**

[![n8n](https://img.shields.io/badge/Workflow-n8n-ff6e5c?style=flat&logo=n8n)](https://n8n.io/)
[![Node.js](https://img.shields.io/badge/Runtime-Node.js-339933?style=flat&logo=node.js)](https://nodejs.org/)
[![Gemini](https://img.shields.io/badge/AI-Google_Gemini-8E75B2?style=flat&logo=google)](https://deepmind.google/technologies/gemini/)
[![Telegram](https://img.shields.io/badge/Chat-Telegram-26A5E4?style=flat&logo=telegram)](https://telegram.org/)

## 📖 Overview

This project is an automated AI Agent designed to keep you updated with the latest developments in Artificial Intelligence without the noise.

Running on an **n8n** workflow server, the agent scrapes/fetches the latest headlines from **TechCrunch** every morning at **7:00 AM**. It then uses **Google's Gemini AI** to analyze, filter, and summarize the articles into a digestible format before sending a briefed report to a private **Telegram** chat.

## n8n Workflow Automation

![IMAGE]()

## 🛠️ Tech Stack

* **Workflow Automation:** n8n
* **Scripting:** Node.js (used within n8n Function nodes for data parsing)
* **LLM Engine:** [Google Gemini API](https://aistudio.google.com/api-keys)
* **Notification Interface:** Telegram Bot API
* **Data Source:** TechCrunch (RSS/Scraping)

### Javascript Code:

```javascript
// 1. Get all items
const allArticles = items;

// 2. Slice the top 5
const top5 = allArticles.slice(0, 10);

// 3. Merge them into one single text block
const combinedText = top5.map(article => {
  return `Title: ${article.json.title}\nSummary: ${article.json.contentSnippet || article.json.content}`;
}).join("\n\n---\n\n");

// 4. Return as a SINGLE item for the AI
return [{
  json: {
    text_to_summarize: combinedText
  }
}];
```

### Installation & Setup

#### 1. Clone or Download
Clone this repository to access the workflow JSON file.
```bash
git clone [https://github.com/yourusername/ai-news-agent.git](https://github.com/yourusername/ai-news-agent.git)

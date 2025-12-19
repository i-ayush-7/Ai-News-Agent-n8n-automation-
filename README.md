# 🤖 Ai News Agent

> **Automated daily AI news briefings delivered straight to Telegram.**

## 📖 Overview

This project is an automated AI Agent designed to keep you updated with the latest developments in Artificial Intelligence without the noise.

Running on an **n8n** workflow server, the agent scrapes/fetches the latest headlines from **TechCrunch** every morning at **7:00 AM**. It then uses **Google's Gemini AI** to analyze, filter, and summarize the articles into a digestible format before sending a briefed report to a private **Telegram** chat.

## n8n Workflow Automation

![IMAGE](https://github.com/i-ayush-7/Ai-News-Agent-n8n-automation-/blob/main/n8n%20workflow%20automation.png)

## 🛠️ Tech Stack

* **n8n Instance:**
* **Scripting:** Node.js (used within n8n Function nodes for data parsing)
* **API Key:** [Google Gemini API](https://aistudio.google.com/api-keys)
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

### Promp:

```text
You are an Executive Tech Analyst. I will provide a list of article titles and descriptions.

1. Identify the 5 most critical stories.

2. Summarize each in one punchy sentence.

3. Ignore clickbait.

4. Start with "🚀 Morning Briefing:"
```

### URL:

```text
https://api.telegram.org/bot<YOUR_BOT_TOKEN>/sendMessage?chat_id=<USER_CHAT_ID>&text=Please Subscribe
```

** Project By: Ayush Shukla ** 

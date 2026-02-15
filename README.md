Perfect 👍
Here is a **GitHub-ready README.md version** — clean, professional, properly formatted, and polished for your repository.

You can directly copy-paste this into your `README.md` file.

---

# 🚀 Daily News to Instagram Image Poster

An automated workflow that fetches daily news headlines, generates AI-powered images, and posts them directly to Instagram — completely hands-free.

---

## 📌 Overview

This project automates the entire process of:

* 📰 Fetching daily top news headlines
* 🤖 Analyzing news using AI
* 🎨 Generating AI images for each headline
* 📲 Posting the content automatically to Instagram

The workflow runs daily at **9:00 AM** and publishes the top 3 news posts with generated captions and images.

---

## 🏗 Workflow Architecture

### ⏰ 1. Trigger

**Node:** `Daily 9 AM Trigger`
Triggers the workflow automatically every day at 9 AM.

---

### ⚙️ 2. Workflow Configuration

**Node:** `Workflow Configuration`

* Sets the current date
* Defines the query for fetching top headlines

---

### 📰 3. Fetch News

**Node:** `Fetch Top News from News API`
Retrieves top US headlines using the News API.

---

### 🤖 4. AI Processing

#### Nodes Used:

* **Analyze News & Generate Prompts**

  * Extracts structured news content
  * Generates optimized image prompts

* **OpenAI Chat Model**

  * Analyzes headlines
  * Creates summaries & captions

* **Structured Output Parser**

  * Converts AI output into structured JSON format

---

### 🔢 5. Limit & Split News

* **Limit to 3 News**
  Ensures only the top 3 headlines are processed.

* **Split News Items**
  Splits each news item for individual processing and posting.

---

### 🎨 6. Image Generation

**Node:** `Generate Image with DALL·E`
Generates AI-based images using the created prompts.

---

### 📦 7. Prepare Instagram Data

**Node:** `Prepare Instagram Post Data`

* Formats caption text
* Attaches generated image
* Prepares payload for Instagram API

---

### 📲 8. Post to Instagram

**Node:** `Post to Instagram`
Publishes content using the Facebook Graph API connected to an Instagram Business Account.

---

## 🔐 Required Configuration

Before running this workflow, ensure the following credentials are properly configured:

* ✅ OpenAI API Key
* ✅ News API Key
* ✅ Facebook Graph API Credentials
* ✅ Instagram Business Account ID

All credentials must be properly added and shared within the automation platform.

---

## 🛠 Tech Stack

* Automation Platform (e.g., n8n)
* OpenAI (Chat Model + DALL·E)
* News API
* Facebook Graph API
* Instagram Business Account

---

## 🎯 Final Output

Every day at 9 AM:

1. Top news headlines are fetched
2. AI generates summaries and image prompts
3. Images are created automatically
4. Top 3 news posts are published to Instagram

Fully automated AI-powered news posting system.


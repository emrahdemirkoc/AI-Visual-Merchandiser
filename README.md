# 📸 AI-Powered Visual Merchandising Agent

> **"From Snapshot to SEO Listing in 8 Seconds." An autonomous agent that sees products, writes descriptions, and manages inventory using GPT-4o Vision & n8n.**

![Workflow Screenshot](screenshot.png)

## 🚨 The Problem
Listing a product on global marketplaces (like Etsy/Amazon) is a bottleneck:
* **Time-Consuming:** It takes ~25 minutes per item to write descriptions, find tags, and enter data.
* **Skill Gap:** Requires advanced English creative writing and technical SEO knowledge.
* **Operational Friction:** Keeping digital listings and physical inventory synchronized is manual and error-prone.
* **Opportunity Cost:** Artisans spend time typing instead of creating.

## ✅ The Solution
This system is an **End-to-End Visual Automation** triggered by a single photo sent via Telegram.
Field staff simply snap a picture of the product. The system uses **Computer Vision (GPT-4o)** to analyze the image (material, style, pattern) and automatically generates high-ranking SEO titles, storytelling descriptions, and tags. Finally, it structures this data and updates the global inventory database.

**Total Operation Time:** ~8 Seconds (vs. 25 Mins Manual).

## 🛠 Tech Stack & Capabilities

| Technology | Function |
|------------|----------|
| **GPT-4o (Vision)** | Computer Vision for analyzing visuals, styles, and materials. |
| **n8n** | Workflow orchestration and API management. |
| **Telegram API** | Acts as the trigger (Input) and the reporting dashboard (Output). |
| **JavaScript (Regex)** | Parsing unstructured AI text into structured JSON data. |
| **Google Sheets** | Cloud-based Inventory Management System (CMS). |

## ⚙️ Workflow Architecture

1.  **Inbound Stream (Telegram):** User sends a raw product photo to the bot.
2.  **AI Vision Engine:**
    * Analyzes visual attributes (e.g., "Knitted wool scarf, burgundy, vintage pattern").
    * Generates an SEO-optimized Title.
    * Writes a persuasive "Storytelling" description.
    * Extracts 13 high-volume niche tags.
3.  **Data Parsing:** The system converts the AI's text block into a clean JSON format.
4.  **CMS & Reporting:**
    * Adds a new row to the **Inventory Database** (Google Sheets).
    * Sends a summary report back to the user via Telegram.

## 🚀 How to Use

1.  Import the `workflow.json` file into n8n.
2.  Connect your **Telegram Bot Token**.
3.  Add your **OpenAI API Key** (Must support GPT-4o / Vision).
4.  Link your **Google Sheets** account for inventory.
5.  Send a photo to your bot and watch the magic happen!

---

### 👤 Author
**Emrah Digital** - *Automation & AI Solutions*
[Visit my Website](https://emrahdemirkoc.com)

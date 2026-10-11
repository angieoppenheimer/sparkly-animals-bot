# 🌍 Global Animal Adoptions

An automated bot that collects **animal adoption listings from around the world** and publishes them to a Telegram channel in **multiple languages**.

The goal of this project is to help animals find a home by increasing the visibility of adoption posts from shelters, rescues, and organizations internationally.

👉 **Telegram Channel:** https://t.me/sparklyanimalsbot

---

## ✨ Features

- 🐾 Collects animal adoption posts from:
  - RSS feeds (international adoption websites)
  - Websites without RSS using HTML scraping
- 🌍 International coverage
- 🌐 Automatic translation into:
  - English 🇬🇧
  - Italian 🇮🇹
  - Spanish 🇪🇸
  - German 🇩🇪
  - French 🇫🇷 
- 🖼️ Smart image handling:
  - Uses feed images when available
  - Scrapes images from websites
  - Falls back to text-only posts if needed
- 🧹 Cleans HTML content (no `<p>`, `<a>`, blog junk, etc.)
- 🚫 Filters out blog posts, news, and technical updates
- 🏷️ Automatic hashtags:
  - Species (#dog, #cat, …)
  - Country (#it, #es, #us, …)
  - Language (#en, #it, #es)
- 🔁 Prevents duplicate posts using SQLite
- ⏱️ Runs automatically with GitHub Actions (every few minutes)
- 💸 100% free hosting (no server required)

---

## 📢 Telegram Channel

All collected adoption posts are published here:

➡️ **https://t.me/globalanimaladoptions**

Feel free to follow, share, and help animals find a loving home ❤️

---

## ⚙️ How It Works

1. GitHub Actions runs the bot on a schedule
2. The bot:
   - Fetches RSS feeds
   - Scrapes selected adoption websites
   - Cleans and translates the content
   - Detects species and country
   - Filters non-adoption content
3. New adoption posts are sent to Telegram
4. Previously posted items are skipped using a persistent SQLite database

---

## 🛠️ Technologies Used

- Python 3.10
- GitHub Actions (automation & scheduling)
- Telegram Bot API
- SQLite (anti-duplicate storage)
- Libraries:
  - `feedparser`
  - `requests`
  - `beautifulsoup4`
  - `langdetect`
  - `deep-translator`
  - `python-telegram-bot`

---

## 🚀 Running Automatically

The bot is designed to run automatically using **GitHub Actions** with a cron schedule.

No VPS, no paid services, no manual intervention required.

---

## ❤️ Contributing

Contributions are welcome!

You can help by:
- Adding new adoption sources
- Improving scraping logic
- Improving language detection or translations
- Reporting bugs or false positives

---

## ⚠️ Disclaimer

This project is intended **only to promote animal adoptions**.  
All content belongs to the original shelters and organizations.

If you manage a shelter and want your content removed or improved, please get in touch.

---
## 🏠 How to Add Your Shelter

If you manage an animal shelter, rescue group, or foster network and would like your adoption posts to appear on **Global Animal Adoptions**, you’re very welcome to join.

### ✅ Preferred Option: RSS Feed
The easiest way to be included is to provide a **public RSS feed** that contains your adoption listings.

Examples:
- WordPress sites usually have a feed at `/feed`
- Dedicated adoption platforms often provide RSS automatically

Please make sure:
- The feed contains **real adoption posts**
- Each post has a **title, description, and link**
- Images are included if possible (optional but recommended)

---

### 🌐 Websites Without RSS
If your website does **not** provide an RSS feed but has a public page listing adoptable animals, it can still be included using **HTML scraping**.

In this case, please provide:
- The exact URL of the adoption page
- Confirmation that scraping is allowed by your website’s terms
- A consistent page structure (list of animals, profiles, etc.)

---

### 🚫 What Is Not Accepted
To keep the channel clean and useful, the following are **not included**:
- Blog posts or technical updates
- News articles or announcements
- Fundraising-only posts
- Event-only pages

The bot automatically filters non-adoption content.

---

### 📩 How to Request Inclusion

To request adding your shelter, please:
- Open a **GitHub Issue** in this repository  
  **or**
- Contact the project owner via email 📧 **angieoppenheimer@protonmail.com**

Include:
- Shelter name
- Website URL
- RSS feed URL (if available)
- Country
- Species you handle (dogs, cats, others)

---

### ❤️ Our Mission
This project exists to **help animals find homes**, not for profit or promotion.

If you represent a shelter and would like improvements, corrections, or removal of your content, just reach out — we’re happy to help.

---

## 🐶🐱 Let’s help animals find a home

If this project helps even one animal get adopted, it’s worth it.

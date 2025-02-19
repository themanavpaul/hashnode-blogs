---
title: "Day 6/30 I Saved a Marketing Firm $5000 With a Weekend Project"
seoTitle: "Saved Marketing Firm $5000 in One Weekend"
seoDescription: "Saved a marketing firm $5000 with ScrapeX, a Twitter scraper providing real-time insights without costly tools. Learn how in this 30-day blog series"
datePublished: Wed Feb 19 2025 15:09:03 GMT+0000 (Coordinated Universal Time)
cuid: cm7c1tn8z000d0al19wgnawrr
slug: day-630-i-saved-a-marketing-firm-5000-with-a-weekend-project
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1739984057724/ae56469a-e203-41fd-aba8-29f159200fe4.png
tags: twitter, python, full-stack, scraping, 10xengineer, generative-ai, genai, 100xdevs, mastergenai

---

# Introduction

A weekend, a few lines of code, a strong cup of coffee, and some classical music—that's all it took to save a marketing firm $5000.

While talking to a marketing agency, I discovered they were spending thousands of dollars on tools to track brand mentions, identify industry trends, and run influencer marketing campaigns. That got me thinking—what if I could build a tool to do all of this for free?

So, I built **ScrapeX**, a Twitter scraper with sentiment analysis, without using Twitter’s paid API. This project not only fetched real-time data from Twitter but also performed sentiment analysis, providing valuable insights for the firm.

Video for better Understanding:

%[https://www.youtube.com/watch?v=xsPSaGd6Lp4] 

---

👋🏻 Hey there! I'm [**Manav Paul**](https://linktr.ee/themanavpaul), a 24-year-young **spiritual developer** with a newfound fascination for generative AI. This blog is my digital diary, where I'll be documenting my exploration of this exciting field. As a curious learner, I'm diving headfirst into understanding the basics, experimenting with different tools, and sharing my insights along the way.

**Here are the projects I recently worked on in generative AI**:

1. [**AI Article Summarizer**](https://chaturai.netlify.app/)**:** Tired of reading lengthy articles? My AI summarizer can do just that.
    
2. [**AI Twin 24/7**](https://manavpaul.hashnode.dev/my-ai-twin-works-247-even-while-i-sleep)**:** Imagine having a digital clone that works 24/7, even while you sleep. I've built one!
    

**Want to learn how?** Dive into my beginner friendly 30-day blog series.

**▶** [**Master GenAI Series**](https://manavpaul.hashnode.dev/series/generative-ai)

---

Let’s Dive in ! 🤿

# The Problem

Marketing firms rely heavily on social media insights, often subscribing to multiple paid services for:

* Tracking brand mentions
    
* Identifying industry trends
    
* Running influencer marketing campaigns
    
* Gaining audience insights
    
* Generating content ideas
    
* Providing real-time customer support
    
* Conducting market research
    

These services come at a hefty price, which smaller firms might struggle to afford. That’s where ScrapeX comes in.

---

# How I Built ScrapeX

I broke the whole process down into **five steps**:

## **Step 1: Load Environment Variables**

**Problem:** Initially, I hardcoded credentials, which was insecure.  
**Solution:** I moved all sensitive details to a **.env file**, making the system secure using the `python-dotenv` library.

## **Step 2: Internet Connectivity Check**

**Problem:** The script failed when the internet connection dropped.  
**Solution:** I added an **asynchronous wait mechanism** to retry every 5 minutes until reconnection.

## **Step 3: Authentication**

**Problem:** Logging in every time was slow and inefficient.  
**Solution:** I **saved session data** in a `cookies.json` file, enabling automatic login without needing credentials each time.

## **Step 4: Fetching Tweets & Handling Rate Limits**

**Problem:** Twitter enforces **strict rate limits**—6000 tweets/day for verified users, 600 for unverified users, and only 300 for newly unverified users. My account was getting blocked.

**Solution:**

* Implemented a **countdown timer** to introduce delays between requests.
    
* Used **randomized delays** (2-5 seconds) to mimic human behavior and avoid detection.
    

## **Step 5: Saving Tweets to CSV**

**Problem:** Previously, every run overwrote existing data, and some tweets lacked necessary fields.  
**Solution:**

* Switched to **append mode** to prevent overwriting.
    
* Added a **try-except block** to handle missing fields gracefully.
    

---

# The Impact

* The marketing firm no longer needs expensive subscription-based services.
    
* ScrapeX provides **real-time Twitter insights** for free.
    
* The firm saved **$5000 per month**, which they can now invest elsewhere.
    

---

# How You Can Use ScrapeX

ScrapeX can be used for:

✅ **Data Analysis**: Analyze sentiment trends over time.  
✅ **Market Research**: Study competitors’ social media engagement.  
✅ **Learning Tool**: Understand Python web scraping and data processing.

## **Features of ScrapeX**

* Fetches tweets from any Twitter user.
    
* Handles **Twitter rate limits** with smart retries.
    
* Ensures **persistent connectivity** and resumes scraping if the connection drops.
    
* Saves data to **CSV format** for easy analysis.
    
* Includes a **threshold date** to stop scraping older tweets.
    
* Implements **error handling** to prevent crashes.
    

---

# Setting Up ScrapeX

## **1️⃣ Prerequisites**

* Ubuntu/Linux or Windows
    
* Python3 installed
    
* Basic knowledge of terminal commands
    

## **2️⃣ Installation & Execution**

#### **Step 1: Install dependencies**

```bash
sudo apt update && sudo apt upgrade
sudo apt install python3-pip python3-venv
```

#### **Step 2: Create & Activate Virtual Environment**

```bash
python3 -m venv my_env_project
source my_env_project/bin/activate  # Linux/MacOS
myenv\Scripts\activate  # Windows
```

#### **Step 3: Install Required Python Libraries**

```bash
pip install python-dotenv requests twikit
```

#### **Step 4: Run ScrapeX**

```bash
python main.py
```

#### **Step 5: Enter Credentials & Twitter Username**

```bash
Enter your Username: <your_twitter_username>
Enter Your E-MAIL: <your_email>
Enter your Password: <your_password>
Enter the Twitter account username to scrape: <desired_twitter_account>
```

---

# **Disclaimer**

This script is provided for **educational purposes only**. It does **not** use the official Twitter API, and scraping methods may change if Twitter updates its structure. Use responsibly.

---

# **What’s Next?**

This was **Part 1**: Building the scraper.

**Coming Next: Part 2 Sentiment Analysis!** 🔥

* Cleaning the dataset
    
* Applying Natural Language Processing (NLP) techniques
    
* Performing sentiment analysis on the scraped tweets
    

🔔 **Stay tuned for the next blog!**

---

## **Connect with Me**

👋 Hi, I’m **Manav Paul**, a 24-year-old **spiritual developer**, passionate about **AI, DevOps, and cybersecurity**. I'm currently diving deep into **Generative AI & Machine Learning**.

📌 **Follow me for more tech insights**:

* **LinkedIn**: [Connect Here](https://www.linkedin.com/in/manav-paul/)
    
* **X (Twitter)**: [Follow Here](https://x.com/themanavpaul)
    

---

🚀 **Want to build your own version?** The complete project is open-source!

Check out the repo: [GitHub Link](https://github.com/themanavpaul/scraperx-twitter-sentiment-analysis)
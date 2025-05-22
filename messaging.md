# 📲 Salesforce Messaging for In-App and Web (MIAW) - Complete Beginner Guide

## 🧠 What Is MIAW?

**Messaging for In-App and Web (MIAW)** in Salesforce is a feature that lets companies offer real-time messaging to users on their website or mobile app. Customers can chat with either:

- An **Einstein Bot**
- A **Live Agent**

This helps deliver faster, contextual, and more personalized support.

---

## ✅ Why Use Messaging in App and Web?

### Business Benefits:

- 💬 Real-time chat for instant help
- 📱 Embedded on website/mobile app – no page switch needed
- 🤖 Supports bots (automated replies) to reduce agent load
- 🔄 Integrated with Omni-Channel for smart routing
- 📝 Full session history for better context and analysis

---

## ⚙️ Architecture Overview

```plaintext
Customer (Web/Mobile)
        ↓
MIAW Chat Widget (JavaScript)
        ↓
Einstein Bot (optional)
        ↓
Omni-Channel Routing
        ↓
Live Agent (in Salesforce Service Console)
        ↓
Conversation saved in Messaging Objects


Key Components:
Embedded Service Deployment: The script you put on your website

Messaging Channel: Connects your website to Salesforce

Einstein Bot: Optional bot that answers FAQs or captures details

Omni-Channel: Routes the message to the right agent

Service Console: Where agents reply

Session Data: Saved in MessagingSession, MessagingUser, and ConversationEntry objects
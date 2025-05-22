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




**# 🛠️ Step-by-Step Guide: Setting Up Salesforce Messaging for In-App and Web (MIAW)
**
This guide explains not just **how** to set up Salesforce Messaging, but also **why** each step matters.

---

## ✅ Step 1: Enable Messaging

**Why:** This activates the Messaging feature in your Salesforce org so you can use chat on websites or mobile apps.

**Steps:**

- Navigate to: `Setup → Messaging Settings`
- Enable **In-App and Web Messaging**

---

## ✅ Step 2: Set Up Omni-Channel

**Why:** Without Omni-Channel, Salesforce won’t know which agent should receive the chat request.

**Steps:**

1. Go to: `Setup → Omni-Channel Settings → Enable`
2. **Create a Service Channel**
   - This defines what kind of work (MessagingSession) is coming in.
3. **Create Routing Configuration**
   - Tells Salesforce how to route work (e.g., 1 agent handles 2 chats).
4. **Create Presence Configuration**
   - Define agent statuses like "Available", "Busy", etc.
5. **Assign Presence Statuses to Users**
   - Enable users to receive work based on their availability.

---

## ✅ Step 3: Create Messaging Channel

**Why:** The Messaging Channel connects your website or app to Salesforce.

**Steps:**

- Go to: `Setup → Messaging Settings → Add Messaging Channel`
- Select **In-App and Web**
- Set the following:
  - **Channel Name**
  - **Website URL** (where the widget will be used)
  - **Deployment** (created in next step)
  - **Bot** or **Queue** to handle chats

> Now Salesforce knows where chats come from and who should handle them.

---

## ✅ Step 4: Create Embedded Service Deployment

**Why:** This generates a JavaScript snippet you add to your website or app.

**Steps:**

1. Go to: `Setup → Embedded Service Deployments`
2. Click **New Deployment** → Choose **Messaging**
3. Link the **Messaging Channel**
4. Customize:
   - Branding (logo, color)
   - Greeting message
5. Copy the generated **JavaScript Snippet**
6. Paste it in your website's `<head>` or `<body>`

> This enables the live chat widget to appear on your site.

---

## ✅ Step 5: Create or Attach an Einstein Bot (Optional but Powerful)

**Why:** Bots can automatically answer common questions, reducing agent workload.

**Steps:**

- Navigate to: `Setup → Einstein Bots`
- Create a new bot or use a template
- Add Dialogs (Greeting, FAQs, Case Lookup, etc.)
- Test and **Publish**
- Attach the bot to the Messaging Channel

---

## ✅ Step 6: Agent Console Setup

**Why:** Agents need the right UI to handle incoming messages.

**Steps:**

1. Go to: `App Builder → Modify/Create a Service Console App`
2. Add **Omni-Channel Utility Bar**
3. Add **Messaging Components** (e.g., Messaging Session Panel)
4. Make sure **Presence Statuses** are visible
5. Train agents on:
   - Going online
   - Accepting chats
   - Using quick replies, notes, and transcript tools

---

## 🧪 Step 7: Testing & Validation

**Steps:**

- Log in as an agent → Set status to **Available**
- Visit the website with the embedded widget
- Initiate a chat
- The **Bot** responds or routes to a **Live Agent**
- Agent receives it via **Omni-Channel**
- Agent chats in real time and ends session

---

## 🔎 Objects Involved in Messaging

| Object Name              | Purpose                                  |
|--------------------------|------------------------------------------|
| `MessagingSession`       | One full session (from start to end)     |
| `MessagingUser`          | Represents the end-user (customer)       |
| `ConversationEntry`      | Each individual message in the session   |
| `ConversationTranscript` | Full conversation record                 |

> These objects can be used for automation, case creation, and analytics.

---

## 📊 Reporting & Analytics

Use **Messaging Insights Dashboards** to track:

- ⏱ Average handle and wait times  
- 🤖 Bot deflection and handoff rate  
- 📥 Queue traffic and agent workload  
- 🌟 CSAT scores (if feedback is enabled)  

> Go to `App Launcher → Messaging Insights

Dialog```
added

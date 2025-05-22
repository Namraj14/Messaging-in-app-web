🔐 Why Consent Levels Matter
When a business sends messages to customers, compliance and privacy laws require that customers have consented to receive those messages.

Salesforce supports four key consent levels:
1. ✅ Implicit Opt-In
🔹 No formal "Yes" or keyword is required from the customer.
🔹 The very act of the customer messaging you first is considered as giving you permission.

📌 Example:
Customer: “Hi, I have a question about my order.”

✔ You are now allowed to message them back on the same channel.

⚠️ Salesforce does NOT send an auto opt-in confirmation for this.

📍 Used in: Web Chat, In-App Messaging, Facebook Messenger, and enhanced channels.

2. 🗣 Explicit Opt-In
🔹 The customer must clearly say YES to getting messages from your company.
🔹 You prompt them, and they must reply with a specific keyword (like "Yes").

📌 Example:
Customer: "Hi, I need help."

You: “Thanks for contacting us! To continue getting messages, reply YES.”

Customer: "Yes"

You: “Thanks! You’ve opted in.”

📍 Used in: Channels like WhatsApp or SMS where laws are stricter.

3. 🔁 Double Opt-In
🔹 A 2-step confirmation is required:

First, customer replies with “Yes”

Then, customer replies again with “Start” (or another confirmation keyword)

📌 Example:
Customer: "Hi"

You: "To get messages from us, reply YES."

Customer: "Yes"

You: "To confirm, reply START."

Customer: "Start"

You: "Thanks! You’ve successfully opted in."

📍 **Used when even more legal assurance is needed.

4. ⛔️ Opt-Out
🔹 Customers can stop receiving messages by sending an opt-out keyword like "STOP".

📌 Example:
Customer: "STOP"

You (auto-response): “You’ve opted out of messages. You won’t receive more unless you message us again.”

📍 Important Notes:

SMS (toll-free): Opt-out cannot be customized — it’s handled by the carrier, not Salesforce.

Facebook Messenger: If the user blocks or deletes the chat, you can’t message them again unless they re-initiate the conversation.

🔁 Re-Opt-In
If a customer opts out and later sends you a message again:

They’re considered to be opted back in.

But for explicit or double opt-in channels, they’ll need to go through the opt-in process again.


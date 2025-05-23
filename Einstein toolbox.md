🗂 Category: Messages
These elements are used to send or receive messages from the user.

| Component                | What it Does                         | Why Use It                  | Example                               | What Happens if You Don’t              |
| ------------------------ | ------------------------------------ | --------------------------- | ------------------------------------- | -------------------------------------- |
| **Message**              | Send a plain message                 | To talk to the user         | "Hi! How can I help you today?"       | Bot won’t greet or respond clearly     |
| **File**                 | Sends a file or attachment           | To share PDFs or forms      | Send a PDF user guide                 | User may not receive needed docs       |
| **Message (Dynamic)**    | Send a message using a variable      | For personalized messages   | “Hello {!UserName}”                   | Messages become generic                |
| **Message (Static)**     | Hardcoded message                    | Fixed text reply            | "Thanks for contacting us!"           | NA – this is default way to speak      |
| **Messaging Components** | Interactive messages like rich cards | For richer UX               | Show buttons/cards with options       | Bot may feel text-only, boring         |
| **Authentication**       | Secure login step for user           | To fetch user-specific data | "Please login to access your account" | Can't show order/account info securely |

🗂 Category: Questions
These are used to ask users for input (text, picklist, etc.).
| Component              | What it Does                    | Why Use It                    | Example                       | What Happens if You Don’t          |
| ---------------------- | ------------------------------- | ----------------------------- | ----------------------------- | ---------------------------------- |
| **Question (Dynamic)** | Ask a question using a variable | For smart data gathering      | "What is your {!FieldLabel}?" | You can't personalize the question |
| **Question (Static)**  | Fixed question                  | Simple, direct asks           | "What’s your email?"          | NA – it’s the default way to ask   |
| **Time Selector**      | Lets user pick date/time        | For appointments/reservations | "Pick your delivery date"     | User might type wrong formats      |


🗂 Category: Actions
These are used to do something (call Flow, Apex, Email, etc.).
| Component              | What it Does                     | Why Use It                       | Example                                 | What Happens if You Don’t               |
| ---------------------- | -------------------------------- | -------------------------------- | --------------------------------------- | --------------------------------------- |
| **Apex**               | Call Apex class                  | For complex logic                | Validate order status with Apex         | Can't run backend logic                 |
| **External Service**   | Call API via External Service    | Integrate with 3rd-party systems | Fetch tracking info from FedEx API      | Bot can't connect with external systems |
| **Flow**               | Run a Salesforce Flow            | Automate business logic          | Create a case or update contact         | You lose no-code automation power       |
| **Goal**               | Track what user wants to achieve | To report on intent success      | "Did user complete ‘Track Order’ flow?" | Hard to measure bot effectiveness       |
| **Knowledge Feedback** | Capture article helpfulness      | For Knowledge articles           | “Was this article helpful?” Yes/No      | Miss feedback from users                |
| **Object Search**      | Search Salesforce records        | Show real-time CRM data          | "Find all open cases for this contact"  | Bot can’t fetch live CRM info           |
| **Send Email**         | Send email to someone            | Notify customers or agents       | "We've sent you a reset link"           | No email confirmation is sent           |

🗂 Category: Standard
These are common controls used to manage flow of dialog.
| Component              | What it Does                | Why Use It                | Example                                            | What Happens if You Don’t             |
| ---------------------- | --------------------------- | ------------------------- | -------------------------------------------------- | ------------------------------------- |
| **Rules**              | Apply logic (if/else)       | Dynamic flows             | If order ID exists, show tracking; else ask for ID | You can’t build smart branching logic |
| **Call Dialog**        | Reuse another dialog        | Avoid repetition          | "Call shipping dialog again"                       | You must copy-paste same steps again  |
| **Clear Variable**     | Reset a value               | Start fresh for next task | Clear OrderNumber after chat                       | Old values might affect new flows     |
| **End Chat**           | Ends the session            | Closes properly           | "Thanks! Ending the chat."                         | Chat remains open — bad experience    |
| **Redirect to Dialog** | Move user to another dialog | Control flow              | After login, send to “Main Menu”                   | User may get stuck                    |
| **Send a Message**     | Same as Message             | Sends a plain text        | "Welcome back!"                                    | NA                                    |
| **Set Language**       | Change chat language        | Multi-language bots       | Switch to Spanish                                  | Responses stay in wrong language      |
| **Set Routing Type**   | Define handoff rules        | To transfer to agent      | Route based on department                          | User may reach wrong agent            |
| **Set Variable**       | Store a value               | To remember info          | Set `OrderID = 12345`                              | You can’t pass data between steps     |
| **Transfer**           | Handoff to agent            | Escalation                | "Let me connect you to support."                   | Bot can’t transfer to live agent      |



🔁 Common Use Cases – Mini Flow Examples
🔷 Example: Track My Order Bot
| Step | Component         | Why                                            |
| ---- | ----------------- | ---------------------------------------------- |
| 1    | Message           | Welcome user                                   |
| 2    | Question (Static) | Ask for Order ID                               |
| 3    | Flow              | Pass Order ID to a Salesforce Flow             |
| 4    | Message (Dynamic) | Show result: "Your order is out for delivery." |
| 5    | End Chat          | Close properly                                 |


🔷 Example: Schedule Appointment
| Step | Component      | Why                              |
| ---- | -------------- | -------------------------------- |
| 1    | Message        | Intro message                    |
| 2    | Authentication | Verify who the user is           |
| 3    | Time Selector  | Ask for appointment time         |
| 4    | Flow           | Create appointment in Salesforce |
| 5    | Message        | Confirm booking                  |
| 6    | End Chat       | End politely                     |

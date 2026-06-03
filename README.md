# Telegram Morning Quote Automation with Make

An automated cloud-native workflow that fetches daily inspirational quotes from the **ZenQuotes API** and delivers them straight to your personal **Telegram Bot** every morning. 


This project is built entirely using **Make.com**.


## Architecture Flow

```text
[ ZenQuotes API ] ──( HTTP GET )──> [ Make.com Engine ] ──( Telegram Bot API )──> [ Your Telegram Chat ]
```

---------------------
## Prerequisites & Telegram Bot Setup

Before importing the blueprint, you need to create your Telegram Bot and retrieve your Telegram account's Chat ID.

### 1. Create a Telegram Bot via @BotFather
1. Open your Telegram and search for **@BotFather** (ensure it has the official blue verification checkmark).
2. Start a chat with him and send the command: /newbot
3. Set up bot username which **must end in "bot"** (e.g., alexa_morning_bot).
4. Save the Token: BotFather will congratulate you and provide a long string of characters called the HTTP API Token (e.g., 748392:AAHfjks...). **Copy and keep this secure**
5. Activate the Bot: Click the link to your new bot provided by BotFather (or search for its username) and click the Start button at the bottom of the chat to activate.

### 2. Get Your Personal Chat ID via @userinfobot
1. In the Telegram search bar, search for @userinfobot.
2. Start a chat with the bot and click Start.
3. Copy the numerical value inside the Id: field (e.g., 123456789). This tells your bot exactly where to send the daily message.


----------------------
## Deploying the Workflow to Make

### 1. Import the Blueprint to Make.com
- Log in to your [Make.com](https://www.make.com/)
- Click the 3-dot icon to import blueprint.json file.

### 2. Configure the Modules
- Double-click at Telegram Bot Module (Telegram sphere icon) and do as follows:
    - Click "Add Connection" and paste the HTTP API Token you obtained from @BotFather.
    - Insert your numerical ID from @userinfobot in the Chat ID field.

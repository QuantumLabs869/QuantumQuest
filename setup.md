Here's the revised `.md` file with the necessary fixes and adjustments:

---

# QuantumQuest Setup Guide

## Installation

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/QuantumLabs869/QuantumQuest
   cd QuantumQuest
   ```

2. **Install Requirements:**
   Ensure you have Python 3 installed. Then, install the necessary packages using:
   ```bash
   pip install -r requirements.txt
   ```

3. **Setup Configuration:**
   Edit the `settings.json` file with the following structure:

   ```json
   {
     "Mode": {
       // Use only one mode at a time to avoid errors
       "account_browser": false,  // Set to true and provide email to start a PC browser session.
       "account_browser_mobile": false, // Set to true and provide email to start a mobile browser session.
       "gen_outlook": false // Set to true to enable Outlook account generation.
     },
     "BrowserSettings": {
       "headless": false, // Set to true to run the browser in headless mode (no GUI).
       "session": true, // Set to false to disable session handling.
       "no_images": true, // Set to false to allow images to load.
       "virtual_display": false, // Set to true to use a virtual display (useful for headless mode).
       "browser": false // Specify the browser to use (e.g., "brave", "edge", "uc"). Set to false for Chrome.
     },
     "tasks": {
       "pc_search": true, // Set to false to disable PC searches.
       "mobile_search": true, // Set to false to disable mobile searches.
       "Daily": false, // Set to true to enable daily tasks.
       "More promotions": true, // Set to true to enable more promotions.
       "Punch cards": true, // Set to true to enable punch cards.
       "Prediction Game": false, // Set to true to enable Prediction Game (note: this task has been removed by Microsoft).
       "Read to earn": false // Set to true to enable "Read to earn" tasks.
     },
     "extension_filenames": [
       "web.crx",  // Filename of the first custom extension to be used.
       "font.crx", // Filename of the second custom extension to be used.
       "audio.crx" // Filename of the third custom extension to be used.
     ],
     "vpn": {
       "enabled": false, // Set to true to enable the inbuilt Windscribe VPN.
       "username": "your_username", // VPN username.
       "password": "your_password", // VPN password.
       "location": "your_desired_location" // VPN location to connect to.
     },
     "BotSettings": {
       "click_results": true, // Set to false to disable clicking search results.
       "scroll_results": true, // Set to false to disable scrolling through search results.
       "repeat_predictiongame": false, // Set to true to repeat Prediction Game if it fails.
       "fast2x": true, // Set to false to disable fast execution.
       "fast4x": false, // Set to true for maximum speed.
       "bonus": true, // Set to false to disable collecting bonus points.
       "nordvpn": false, // Set to true to use NordVPN instead of Windscribe.
       "captcha": true, // Set to false to disable CAPTCHA solving.
       "skip_unusual": false, // Set to true to skip detection of unusual activity.
       "shuffle": true, // Set to false to disable shuffling accounts.
       "skip_if_proxy_dead": true, // Set to false to avoid skipping dead proxies.
       "print_to_webhook": true, // Set to false to disable printing messages to a webhook.
       "TOKEN": "your_token", // Telegram bot token; set to false if not using Telegram.
       "CHAT_ID": "your_chat_id", // Telegram chat ID; set to false if not using Telegram.
       "Discord_url": "webhook_url", // Discord webhook URL; set to false if not using Discord.
       "recheck_proxy": true, // Set to false to disable rechecking proxy status.
       "start_at": "HH:MM", // Time to start the script (24h format); set to false if not using.
       "accounts_file": "genoutlook.json", // File containing accounts; set to false to use the default accounts.json.
       "search_interval": 7, // Time interval between searches in seconds.
       "accountLimit": 10, // Number of accounts to create; only works if gen-outlook mode is enabled.
       "gen_country": "Your country", // Country to generate accounts from.
       "2captcha_api": "your api", // 2Captcha API key; remove this line or set to false to use the free version.
       "redeem_goal": 1700, // Points goal for redemption.
       "RedeemAssistant": "skip", // Choose from: "skip", "tasks", "searches", "searchesR". "Skip" skips accounts until manual removal from redeem.txt.
       "secondary_email": "your_secondary_email@example.com" // Secondary email for the bot; only applicable when secondary mode is enabled.
     }
   }
   ```

4. **Account Management:**
   - **Add Accounts:**
     Place existing accounts in the `Accounts` folder.
     For account management, use `genoutlook.json`. You can either specify the accounts file with:
     ```bash
     "accounts_file": "genoutlook.json"
     ```
     (recommended using `accounts-file genoutlook.json`)
     Or generate accounts using:
     ```bash
     {
        "Mode": {
       "gen_outlook": true
     }
     ```

## Running the Script

Once everything is set up, you can run the script with your desired settings:
```bash
python main.py
```

### How to Run `gen-outlook`:

1. Ensure your `settings.json` includes the following configuration to enable account generation and set account limits:

   ```json
   {
     "Mode": {
       "gen_outlook": true
     },
     "BotSettings": {
       "accountLimit": 10,
       "gen_country": "Your Country",
       "accounts_file": "genoutlook.json"
     }
   }
   ```

2. Execute the following command:
   ```bash
   python main.py
   ```

2.1 **How to Use Proxies in `gen-outlook`**

Manage proxies using `proxies.json`:

- **Authenticated Proxy:**
  ```json
  {
    "proxy": "http://proxy-url:port",
    "proxy_auth": "username:password"
  }
  ```

- **Non-Authenticated Proxy:**
  ```json
  {
    "proxy": "http://proxy-url:port",
    "proxy_auth": null
  }
  ```

- **No Proxies:**
  ```json
  {
    "proxies": []
  }
  ```

## Notes

- **VPN:** Currently, Windscribe is being tested with the extension in the beta version.
- **NordVPN:** Available for those with a NordVPN account.
- **Extensions:** Add or remove extensions as needed.

For further assistance or issues, contact via Telegram: [click here](https://t.me/QuantumLabs869_bot).

---

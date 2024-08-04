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
   edit the `settings.json` file with the following structure:

   ```json
   {
     "search_interval": 7,  // Time between each search in seconds
     "accountLimit": 10,    // Number of accounts to create by gen-outlook 
     "redeem_goal": 1700,   // Points goal for redemption
     "tasks": {
       "Daily": true,
       "More promotions": true,
       "Punch cards": true,
       "Prediction Game": false,  // Prediction Game removed by Microsoft
       "Read to earn": true
     },
     "extension_filenames": [ // coustom extensions
       "web.crx",
       "font.crx",
       "audio.crx"
     ], // windscribe vpn extension (beta version)
     "vpn": {
       "enabled": false,
       "username": "your_username",
       "password": "your_password",
       "location": "your_desired_location"
     },
     "TOKEN": "your_token", // telegram tocken and chat id
     "CHAT_ID": "your_chat_id",
     "Discord_url": "webhook_url", //add you discord webhook urk
     "secondary_email": "your_secondary_email@example.com" // give a email so bot can use it as secondary email 
   }
   ```

4. **Account Management:**
   - **Add Accounts:**
     Place existing accounts in the `Accounts` folder.
     For account management, use `genoutlook.json`. You can either specify the accounts file with:
     ```bash
     --accounts-file genoutlook.json
     ```
     (recommended using --accounts-file genoutlook.json)
     Or generate accounts using:
     ```bash
     --gen-outlook
     ```

## Argument Details

Here’s a breakdown of each argument you can use with the script:

- `--usa`: Award bonus points for the USA only and to generate usa region account while generating accounts (default set to india)
- `--secondary`: add secondary email addresses 
- `--gen-outlook`: Generate Outlook accounts.
- `--click-results`: Click on search results.
- `--scroll-results`: Scroll through search results.
- `--repeat-predictiongame`: Repeat Prediction Game if it fails (currently removed by Microsoft).
- `--everyday`: Run the script every day at the specified start time.
- `--headless`: Enable headless mode for the browser. not recommended to use
- `--session`: Create a session for each account and use it.
- `--fast`: Reduce delays to speed up the script.
- `--superfast`: Further reduce delays for maximum speed.
- `--discord <WEBHOOK_URL>`: Send logs to Discord via webhook.
- `--account-browser <account>`: Open a browser session for the specified account.
- `--bonus : collect bonus points
 including setting goal(200) etc.
- `--account-browser-mobile <account>`: Open a mobile browser session for the specified account.
- `--start-at <HH:MM>`: Start the script at the specified time (24h format).
- `--on-finish <ACTION>`: Define an action to perform when the script finishes (shutdown, sleep, hibernate, exit).
- `--nordvpn`: Use NordVPN for VPN.
     currently only supported in windows 
- `--skip-unusual`: Skip unusual activity detection.
- `--no-images`: Prevent images from loading to increase performance.
- `--shuffle`: Randomize the order of accounts.
- `--no-webdriver-manager`: Use a system-installed WebDriver instead of `webdriver-manager`.
- `--virtual-display`: Use PyVirtualDisplay 
- `--skip-if-proxy-dead`: Skip accounts if the provided proxy is not working.
- `--print-to-webhook`: Print every message to a webhook.
- `--recheck-proxy`: Recheck proxy status if facing errors.
- `--accounts-file <FILE_NAME>`: Specify the accounts file in the bot directory.
- `--browser <BROWSER>`: Choose the browser to use (options: brave, edge, uc..etc).

## Running the Script

Once everything is set up, you can run the script with your desired arguments. For example:
```bash
python main.py --no-webdriver-manager --fast
```

## Notes

- **VPN:** Currently, Windscribe is being tested with the extension in the beta version.
- Nord vpn available for those who has account in Nord vpn
- **Extensions:** Add or remove extensions as needed.

For further assistance or issues, contact via Telegram: [click here](https://t.me/QuantumLabs869_bot).

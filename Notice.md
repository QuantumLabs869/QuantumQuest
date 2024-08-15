🚀 QuantumQuest 3.2 Beta Launching Today! 🚀

The most human-like bot experience yet with features like typo ,scrolling, random clicks, and wait times! QuantumQuest 3.2 Beta is coming today with an exciting new feature: gen-outlook.

🔹 Introducing gen-outlook:
- Generate Unlimited Outlook Accounts: Create as many Outlook accounts as you need, with details saved in the genoutlook.json file.
- Auto Captcha: No more captcha hassles! We're using the free version of Nopecha with 60%-70% accuracy. A new captcha solver is in the works for the next version. For now, you might need to assist Nopecha with solving captchas.

🔧 How to Run gen-outlook:
python main.py --gen-outlook --no-webdriver-manager --accounts-file genoutlook.json --secondary --captcha --session 

- --secondary: Automatically adds a recovery email to the new accounts. [More info](https://github.com/QuantumLabs869/QuantumQuest/blob/master/FAQ.md)
- --session: Saves the session of the new account, so no need for re-login.
- --captcha: Solves captchas for you.
- --bonus: New accounts will receive all available bonus points on Microsoft.
- Ensure the key "gen_country" is set to your country as recognized by Microsoft, to avoid potential errors in the following format in settings.json:

```json
{
    "gen_country": "Your Country"
}```

Stay tuned for the launch and be among the first to test our latest features!

For questions or support, check out our [FAQ](https://github.com/QuantumLabs869/QuantumQuest/blob/master/FAQ.md).

# QuantumQuest FAQ

<details>
<summary>Q1: **Is the Outlook Account Creator currently working?** </summary>

**A1:** The Outlook Account Creator feature is temporarily down for security reasons. We are working on it, and it will be available again soon.

</details>

<details>
<summary>Q2: How does QuantumQuest bypass the cooldown on searches?
what's Round?
</summary>

**A2:** QuantumQuest checks if your account has a cooldown. If there isn’t one, it slows down the search speed, introduces intentional mistakes in search queries, clicks on search results, and scrolls through them. Additionally, it performs a random number of extra searches (between 2 to 6).

If your account does have a cooldown, the searches are split into rounds with a 15-minute interval between each. During this interval, the bot will handle other accounts and return to the original one after the cooldown period. This ensures no time is wasted.if all other accounts has been finished before 15 minutes it'll wait (15-(total time taken to finish all accounts))

</details>

<details>
<summary>Q3: Can I control the search speed?</summary>

**A3:** Yes, you can adjust the time interval between searches. Based on our experiments, a 7-second delay is recommended for optimal results.

</details>

<details>
<summary>Q4: Is there a parallel mode for running multiple accounts simultaneously?</summary>

**A4:** QuantumQuest does not have a built-in parallel mode due to the risk of account bans when running multiple accounts at once. However, you can run accounts in parallel by copying the bot’s folder, adding a new set of accounts, and running them separately. If you need assistance with this setup, we’re here to help.

</details>

<details>
<summary>Q5: Can I add extensions, like a privacy extension to QuantumQuest?</summary>

**A5:** Yes, QuantumQuest allows you to add browser extensions. Simply update your `settings.json` file with the extensions you want to include.

</details>

<details>
<summary>Q6: Does the Outlook Account Creator handle captchas?</summary>

**A6:** Yes, the Outlook Account Creator includes a captcha solver with approximately 70% accuracy.

</details>

<details>
<summary>Q7: What does the "redeem.txt" file do?</summary>

**A7:** The `redeem.txt` file lists accounts that have reached your specified "redeem goal points," which is set in the `settings.json` file. Once an account reaches the goal, the bot will stop farming for 3 days(it's recommended to give that account a 3-day break) so you can redeem safely. After redeeming remove the account from the list.

</details>

<details>
<summary>Q8: What does the bonus feature do?</summary>

**A8:** The bonus feature is designed to optimize the point accumulation process for fresh accounts. If your account was just added or created, and the bonus argument is included, the bot will:

- **Set an initial goal** of 200 points.
- **Perform Bing searches** for the first level, aiming for 50 points.
- **Complete the TakeLessons signup** task to earn 200 points (currently in beta, so your feedback would be valuable).
- **Skip the maps bonus task** of 100 points. as it has been taken down by Microsoft. The bot will automatically bypass this until the feature is restored.

This approach helps new accounts gain points quickly and efficiently.

</details>

<details>
<summary>Q9: How does the bot add secondary mail to accounts with unusual activity detected?</summary>

**A9:** If you have the `--secondary` option enabled, whenever the bot detects unusual activity on an account, it will add your given email as a secondary email using the "dot trick." This involves adding a dot at a random position in your email, making it appear as a different email address. The bot will then prompt you to enter the OTP in the terminal, so you'll need to keep an eye on the process while using the `--secondary` feature.

</details>

---

For more questions or support, feel free to reach out to us on Telegram! [Contact Us](https://t.me/QuantumLabs869_bot)

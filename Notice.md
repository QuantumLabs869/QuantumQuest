### Redeem Assistant: A Game Changer for Microsoft Farming

Introducing the **Redeem Assistant**—our latest and most powerful feature designed to tackle issues commonly faced during the redemption process, such as the "Try again after 24 hours" error or other order-related problems.

#### How It Works

In the `settings.json` file, under the `RedeemAssistant` section, you can choose from several methods to help resolve these issues:

- **skip**: This option will skip accounts after they reach their goal until you manually remove them from `redeem.txt`. It might help the issue to resolve over time.
  
- **tasks**: The bot will perform additional promotions and daily tasks, then skip the account for the day. This method could also help alleviate issues.

- **searches**: The bot will perform 3-4 searches and then skip the account. This approach may help resolve redemption issues.

- **searchesR**: The bot will perform 3-4 searches in every round (from 1 to 17). This method is highly effective at addressing issues.

**Note**: You can combine multiple methods as long as `skip` is not one of them.
Also don't forget to update your settings.json from GitHub to use without errors 


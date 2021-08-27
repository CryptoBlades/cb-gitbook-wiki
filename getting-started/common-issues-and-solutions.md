# Common Issues and Solutions



## 0.285 Gas Fee

Whenever the user performs a transaction that isn't allowed by the contract, such as adding a 5th character, or trading away a trade locked weapon, they will get asked for a gas fee of 0.285 BNB.

Do not accept these transactions. Carefully evaluate what it is you're doing and confirm that your transaction is legal.

## EVM Error

Users have reported getting EVM errors mostly when performing fights before the hourly reset is done.

The enemy list refreshes every hour at UTC +0, and during the refresh the old enemy list disappears. If a fight transaction is in the middle of being calculated during this, the reference to the old enemy is lost and the transaction fails.

To avoid this, you can stop fighting before the hour is done to avoid any failed fight transactions and wait for the refresh to finish.

## Getting Started Page Stuck

![](../.gitbook/assets/welcome-page.png)

To get past the initial welcome page, a minimum amount of $XWeapon is required to be present in your wallet indicated by the cost to recruit your first character.

Please proceed to the following page to learn how to purchase $XWeapon:

{% page-ref page="purchasing-skill.md" %}


# Fighting

Combat serves as the primary source of gaining SKILL through the use of your character and weapon NFTs. Fighting consists of the player selecting a character and a weapon, and selecting an enemy from a randomized set based on your calculated power.

The overview of the combat formulas can be found here:

{% page-ref page="combat-formula.md" %}

After the player has selected their enemy, the contract calculates on-chain the randomized player and enemy rolls and determines a victory if the player's roll is equal to or higher than the enemy's roll.

A victorious fight results in a experience payout to your character, and a SKILL payout to your in-game wallet.

A defeat results in a loss of the gas fees paid.

Calculations to determine the experience and SKILL payouts can be found here:

{% page-ref page="combat-rewards.md" %}


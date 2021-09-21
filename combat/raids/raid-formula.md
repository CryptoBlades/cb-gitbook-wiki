# Raid Formula

## Player Power

The formula to calculate the power values of each set of character and weapon is identical to the formula used to calculate the player's aligned power in regular fights, without the ±10% variable roll.

Refer to the **Aligned Character Power** section in the following link to calculate the player's power variable found here:

{% page-ref page="../fighting/calculating-player-power.md" %}

After calculating the player's power, the elemental trait of the character is then compared to the raid boss's element to determine if a 1.075 multiplier bonus is applied.

{% hint style="info" %}
Note that unlike regular combat, players do not face a power penalty when going against a raid boss that has an elemental advantage against their selected character. They simply forfeit the 1.075 multiplier bonus and contribute less power to the overall raid.
{% endhint %}

Once all the power has been calculated and the multiplier has been evaluated, that final power value gets added to the raid's total power value for players.

## Raid Success Chance

Calculating the success chance of a raid is a simple RNG roll that compares the total power of all players in the raid compared to the boss's listed power.

We start by randomizing a value which we will call **Player Roll.**

Player Roll is a random number between 0 and the sum of the listed Total Power and Boss Power of the raid.

Player Roll is then compared to Boss Power, and if the randomized roll is greater than Boss Power, the raid is won.

{% hint style="info" %}
This formula means that simply overtaking the listed Boss Power does not guarantee a win. Having equal or near equal Total Power and Boss Power values only means a 50% chance of the raid's success.
{% endhint %}


# Combat Formula

## Combat Variables

Combat in CryptoWar utilizes a set of variables calculated from the NFT data the player owns. These variables are outlined as follows.

* **Unaligned Character Power** is calculated using the character's current level, and the selected weapon without considering any elemental matching.
* **Aligned Character Power** calculated the same as above, except it takes into account if any attributes match the character's element, or if the attribute is PWR.
* **Trait Bonus** is calculated by checking the element of the character and evaluating if it is strong, neutral, or weak against the chosen enemy's element.
* **Enemy Power** is the listed power value of the chosen enemy, and is used in determining the enemy's combat roll and the rewards payout.

Using the above information, we can draw several conclusions for CryptoWar combat that are written out below.

## Elemental Matching

Choosing an enemy that you have an elemental advantage against, comparing a weapon's element to your character, and comparing a weapon's attributes to your character are the three considerations in regards to elemental matching.

Based on the formulas for combat, we can make several key definitive statements.

* Matching elements is important for win rate and experience gain calculations.
* Matching elements is NOT important in calculating enemy power range.
* Matching elements is NOT important in calculating $XWeapon payout.

## Formulas

Combat starts by determining the **Unaligned Character Power** and using that to determine the range of enemies to choose from.

The formula to get that and other variables can be found here:

{% page-ref page="calculating-player-power.md" %}

Once the **Unaligned Character Power** has been determined the game takes that value and applies a ±10% to determine the range of possible enemy power values.

{% hint style="info" %}
This ±10% means you will never receive an enemy that is impossible to beat, though you might be hard pressed to win against an enemy if you don't have the advantage of elemental matching on your side.
{% endhint %}

The player then proceeds to choose an enemy to fight and confirms the transaction. The contract calculates for the player's **Aligned Character Power** and **Trait Bonus** and uses those values to determine the player's combat roll and the experience gained on victory.

The player's roll is calculated by multiplying **Aligned Character Power** with **Trait Bonus** and applying a ±10%.

The enemy's roll is calculated by taking their listed power value and applying a ±10%.

If the player's roll is equal to or greater than the enemy's roll, they win the fight. Experience and SKILL payouts can then be calculated. The formulas used to get those can be found here:

{% page-ref page="combat-rewards.md" %}


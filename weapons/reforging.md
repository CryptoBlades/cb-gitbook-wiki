# Reforging

![](../.gitbook/assets/reforge.png)

Reforging weapons is the process of spending SKILL tokens to burn one weapon into another. The target weapon receives bonus power, and the burned weapon disappears.

Alongside weapon forging, reforging serves as one of the two SKILL sinks in the game. Reforging also gives value to the massive amounts of one to three star weapons that a player may receive when trying to forge for four or five stars.

## LB, 4B, and 5B

![](../.gitbook/assets/reforge-lb-4b-5b.png)

A reforged weapon displays new information when hovered over. This is the LB, 4B, 5B, and Bonus Power.

LB stands for _Low Star Burn_ and is the total value of one to three star weapons burnt.

4B stands for _Four Star Burn_ and is the total value of four star weapons burnt.

5B stands for _Five Star Burn_ and is the total value of five star weapons burnt.

## Bonus Power

![](../.gitbook/assets/reforge-bonus-power.png)

Bonus Power is a new stat gained when reforging that is used alongside weapon attributes to determine player power for combat rolls.

More information on how Bonus Power is used can be found here:

{% page-ref page="../combat/fighting/" %}

## Burn Value

The rarity of the burnt weapon determines which burn pool the value goes to, and for the case of LB determines the amount of burn points to add.

LB, 4B, and 5B have a maximum limit independent of one another, and each point increase in each respective pool contributes to the weapon's total Bonus Power.

Refer to the following table for maximum amount of burn points and the bonus power per point received.

| Burnt Weapon Rarity | Pool | Maximum Pool Value | Bonus Power Per Point | Maximum Bonus Power |
| :--- | :--- | :--- | :--- | :--- |
| 1-star, 2-star, 3-star | LB | 100 | 15 | 1500 |
| 4-star | 4B | 25 | 30 | 750 |
| 5-star | 5B | 10 | 60 | 600 |

This means that a fully reforged weapon can have a maximum of 2850 bonus power.

## Burn Conditions

Depending on the rarity of the weapon and the current value of the pool, the amount increased per burn may change.

Refer to the following to determine how much the pool will increase when the respective weapon rarity is burnt.

* 1-star weapon burns increases LB by two if the LB is under 10, otherwise it increases it by one.
* 2-star weapon burns increases LB by two if the LB is under 30, otherwise it increases it by one.
* 3-star weapon burns increases LB by four if the LB is under 50, otherwise it increases it by two.
* 4-star weapon burns always increases 4B by one.
* 5-star weapon burns always increases 5B by one.

{% hint style="info" %}
Due to the conditions present in LB reforging under 50/100 LB, the optimal way to reforge a weapon starting from 0/100 LB is as follows.

1. Burn five 1-star weapons to increase the LB from 0 to 10.
2. Burn ten 2-star weapons to increase the LB from 10 to 30.
3. Burn five 3-star weapons to increase the LB from 30 to 50.
4. From 50/100 LB onwards you may burn your choice of 1 to 3 star weapons.
{% endhint %}

## Reforge Value

Because the Bonus Power variable added by reforging isn't multiplied by either the character's current power or the weapon, we can calculate the estimated payout increase we get assuming a certain amount of Bonus Power.

The formula to calculate the increased gains will not return a specific amount, but rather a range of values that still depends on the player's choice of enemy.

We start by getting two variables which we'll name **minAddedPower** and **maxAddedPower**. These two variables are obtained by applying a ±10% to the Bonus Power variable.

{% hint style="info" %}
Assuming the following variables:

* Bonus Power : 1500

We get the following:

* minAddedPower : 1350
* maxAddedPower : 1650
{% endhint %}

We then apply the SKILL payout formula to these two variables to determine the range of minimum added payout and maximum added payout.

More information on calculating SKILL payouts can be found here:

{% page-ref page="../combat/fighting/combat-rewards.md" %}

{% hint style="info" %}
Continuing from our example above we apply the payout formula and get the following variables:

* SKILL per 1000 Power : 0.014651 \(taken on July 7, 2021\)
* Minimum Added Payout : 0.01977885
* Maximum Added Payout : 0.02417415

The actual added payout still depends on the enemy power chosen, but with this calculation we have an idea on the range of added payout given by Bonus Power.
{% endhint %}


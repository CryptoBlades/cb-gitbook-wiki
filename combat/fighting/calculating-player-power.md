# Calculating Power

## Unaligned Character Power

Unaligned Character Power is the variable used to determine the range of enemy power rolls.

The required variables to calculate this are the following:

| **Variable** | . | **Description** |
| :--- | :--- | :--- |
| **Character Power** | . | **Character Power** is the listed power displayed on the upper left hand side of the screen above the stamina bar when a character is selected. |
| **Weapon Attribute Base** | . | **Weapon Attribute Base** is the sum of all the weapon's attribute values without taking into consideration elemental matching. |
| **Weapon Bonus Power** | . | **Weapon Bonus Power** is the listed bonus power value if the weapon has been reforged. |

The current formula to calculate for unaligned power is

$$
unalignedPower = (((attributeTotal * 0.0025) + 1)
 * charPower) +bonusPower
$$

After we calculate for unaligned power, we apply a ±10% to determine the range of values that the enemy power values might be.

{% hint style="info" %}
Let's do a sample calculation assuming the following values below:

* Character Power - 1000 \(a level one character\)
* Attribute Total - 800 \(a max attribute 4-star weapon\)
* Bonus Power - 1500 \(a 100/100 LB, 0/25 4B, 0/10 5B weapon\)

Unaligned Power comes out at 4500.

Minimum Enemy Power is 4500 \* 0.9 rounded down to 4050.

Maximum Enemy Power is 4500 \* 1.1 rounded down to 4950.
{% endhint %}

## Aligned Character Power

Aligned Character Power is the variable used in determining the player's combat roll in conjunction with Trait Bonus.

The required variables to calculate this are similar to Unaligned Character Power above but instead of

| **Weapon Attribute Base** | . | **Weapon Attribute Base** is the sum of all the weapon's attribute values without taking into consideration elemental matching. |
| :--- | :--- | :--- |


Aligned Character Power uses

| **Weapon Attribute Multiplied** | . | **Weapon Attribute Multiplied** is the sum of all the weapon's attribute values after applying a multiplier to each attribute based on elemental matching. |
| :--- | :--- | :--- |


Instead of the formula simply summing up all the weapon's attributes, we instead evaluate each attribute separately and apply the following calculations to determine their value

```text
if attributeElement == charElement (attributeValue * 0.0025)
if attributeElement == PWR (attributeValue * 0.002575)
if attributeElement != charElement (attributeValue * 0.002675)
```

Once each attribute has been evaluated, they get totaled and used in the same formula as unaligned power to get the aligned power.

$$
alignedPower = ((evaluatedAttributeTotal + 1) * charPower) + bonusPower
$$

{% hint style="info" %}
Let's do another sample calculation assuming the following values below:

* Character Power - 1000 \(a level one character\)
* Character Element - Fire
* Attribute One - STR 400
* Attribute Two - CHA 400
* Bonus Power - 1500 \(a 100/100 LB, 0/25 4B, 0/10 5B weapon\)

Aligned Power comes out to 4570.
{% endhint %}

Aligned Power is used as is when calculating experience gain, or multiplied with Trait Bonus when calculating the player's combat roll.

## Trait Bonus

![](../../.gitbook/assets/trait-bonus.png)

Trait Bonus is a variable multiplied to Aligned Power and used to determine the player's combat roll.

The formula to determine Trait Bonus is outlined below.

```text
TraitBonus = 1
if charElement == weaponElement (TraitBonus += 0.075)
if charElement > enemyElement (TraitBonus += 0.075)
if charElement < enemyElement (TraitBonus -= 0.075)
```

The elemental advantage in regards to character against enemy is as follows:

* Fire beats Earth
* Earth beats Lightning
* Lightning beats Water
* Water beats Fire

Trait Bonus gets evaluated and then multiplied with Aligned Power to get the players final power value.

A ±10% is then applied to the final value to determine the player's combat roll.

{% hint style="info" %}
Taking the Aligned Power calculated above, let's assume the following variables:

* Character Element - Fire
* Weapon Element - Water
* Enemy Element - Earth

Trait Bonus comes out to 1.075.

Final Power Value after applying Trait Bonus to the Aligned Power above is 4912.

Minimum Player Roll is 4912 \* 0.9 rounded down to 4420.

Maximum Player Roll is 4912 \* 1.1 rounded down to 5403.
{% endhint %}

## Enemy Power

Enemy Power is a simple ±10% calculation applied to the listed enemy power of whatever enemy the player chose.

The numerical value listed on the combat screen button is used to determine experience and SKILL payouts.

The calculated value with the ±10% applied is used to determine the enemy's rolls in combat

{% hint style="info" %}
Taking the previous values into account, let's finalize the sample combat simulation

* Minimum Enemy Power = 4050
* Maximum Enemy Power = 4950

Let's assume the player chose an enemy with a listed power value of 4700.

* Enemy Power = 4700

Minimum Enemy Roll is 4700 \* 0.9 rounded down to 4230.

Maximum Enemy Roll is 4700 \* 1.1 rounded down to 5170.

From this information, we know that the player can roll between 4420 - 5403 and the enemy can roll between 4230 - 5170.
{% endhint %}


# DiabloCalculator
An attempt at replicating Diablo 4's damage calculation formula, with options for enemy type specification and more.
7/11/23

A common term that will be used is 'Damage Buckets'. 'Damage Buckets' are how the community generally classifies multipliers.
There are several multipliers: 'Additive Modifiers', 'Vulnerable Damage Bonus', 'Critical Strike Damage', 'Main Stat Damage Bonus' and 'Global Multipliers'.
Within all of these is naturally a sub-category of conditional modifiers that only activate on certain conditions.
It is like a combination of additive multipliers and their over-arching type.

**'Additive Multipliers'**
(Vs Bleeding + Vs CC + Vs Close + Vs Distant + Vs Elites + Vs Healthy + Vs Injured + Vs Knocked Down + Vs Slowed + Vs Stunned + while Fortified + while Healthy + with Core)
The sum of all of these values will equate to one multiplier which is then applied to your Base Damage.

**'Vulnerable Damage Bonus'**
Vulnerability by default increases the amount of damage an enemy takes by 20%. The total 'Vulnerable Damage Bonus' is then added to that baseline of 20%.
You can tell an enemy is vulnerable when their HP Bar is Purple.

**'Critical Strike Damage'**
Not all skills/abilities/weapons can Crit. Those that can, have a 5% chance of causing a 'Critical Strike' by default.
This chance can be increased by Skill Passives, Aspects, Class Stats and Sub-Stats from Gloves and Rings.
Namely, all DoT Skills do not have a chance to Crit. (Unless stated otherwise.)
When a Critical Strike occurs, the damage numbers will be shown in Yellow.

**'Main Stat Damage Bonus'**
Each class has a main stat associated with them.
Rogue - Dexterity
Sorcerer - Intelligence
Barbarian - Stremgth
Druid - Willpower
Necromancer - Something I'm sure

**'Global Multipliers'**
These are skill effects, generally found in Aspects, Paragon Glyphs. They will usually have a [x] in their tooltip.
An example would be 'Deal 25%[x] [15-25%]% increased damage while you have a **Barrier** active.'

**Overpower**
This is the last multiplier in the equation and adds one final boost to your damage.
This is an additive increase rather than a multiplier.
(HP + Fortified HP + Overpower Damage Bonus)
The base chance of hitting an Overpower is 3% with no other means to improve it.
Certain Aspects, Skills and other things can guarantee Overpower hits however.

If Overpowered and Critical Strike occurs in one instance of damage, it is called 'Critical Overpowered'
'Overpowered Hits' are blue, while Orange numbers indicate 'Critical Overpowered Hits'.

Factoring in all of this, the base damage formula is as follows:
'Base Damage' * 'Total Additive Bonus' * 'Vulnerable Damage Bonus' * 'Total Critical Strike Damage' * 'Main Stat Damage Bonus' * 'Global Multipliers' * 'Overpower Damage'


To complicate things even further, it is not as if every class attacks at the same rate.
There is a 'Weapon Speed' Stat, but some skills are not influenced by this.
For example, 'Whirlwind' has a set-locked animation length.
With this said- by the game's definition, all attacks are **'Skills'**, even Basic Attacks.
Therefore, having an increased Weapon Speed does benefit Energy Generation which results in more comfortable skill rotations.

When wielding one-handed weapons, their attack speed is averaged between the two.



# Beer Design

## Purpose

Beer is the central risk/reward system of the game.

The team kills enemies.

Enemies drop beer.

The Shooter drinks beer.

The Shooter becomes more powerful.

The Rider's job becomes more difficult.

The team must decide:

> **How much power can we handle?**

The core relationship is:

```text id="d4q1g8"
Kill Enemies
    ↓
Obtain Beer
    ↓
Drink Beer
    ↓
Shooter Becomes Stronger
    ↓
Vehicle Becomes More Difficult to Control
    ↓
Team Faces Greater Risk
    ↓
More Enemies Must Be Killed
```

Beer should connect:

* Combat
* Progression
* Cooperation
* Risk
* Vehicle handling
* Comedy

---

# The Core Beer Fantasy

The ideal experience is:

> **We are becoming stronger because we are making increasingly irresponsible decisions.**

The team should not simply think:

> **Beer gives us a buff.**

They should think:

> **We are already drunk. Should we really drink more?**

And then:

> **Yes.**

---

# Beer as a Shared Problem

Beer primarily benefits the Shooter.

However, intoxication affects the entire team.

This creates a natural conflict.

```text id="f17s6n"
Shooter Wants:
More Power

Rider Wants:
More Control
```

The team must negotiate.

Example:

> **Shooter:** "Give me the beer."

> **Rider:** "Absolutely not."

> **Shooter:** "I need more damage."

> **Rider:** "You are already aiming at the floor."

> **Shooter:** "I can handle one more."

This disagreement should emerge naturally from the mechanics.

---

# Beer Acquisition

Beer should primarily be obtained through gameplay.

Possible sources:

## Enemy Drops

Basic enemies may occasionally drop beer.

---

## Elite Enemies

Elite enemies provide larger beer rewards.

---

## Special Enemies

Some enemies may specifically carry or generate beer.

---

## Environmental Objects

Examples:

* Beer crates
* Vending machines
* Bars
* Shops
* Refrigerators

---

## Special Events

The team may encounter opportunities to obtain large amounts of beer.

These opportunities should involve risk.

---

# Beer Should Be a Physical Object

Beer should ideally exist in the game world as something the team must interact with.

Possible forms:

* Bottles
* Cans
* Kegs
* Beer crates

The physical representation is important because it creates spatial decisions.

The team may need to:

```text
See Beer
    ↓
Decide It Is Worth Taking
    ↓
Move Toward It
    ↓
Collect It
    ↓
Escape
```

This gives the Rider a role in beer acquisition.

---

# Beer Collection

The team should not automatically receive every beer drop.

Beer should create decisions about movement.

Example:

```text id="5s2w1h"
Beer Drops
    ↓
Team Sees It
    ↓
Rider Decides Whether to Approach
    ↓
Shooter Decides Whether to Drink
```

This creates two separate decisions:

> **Can we safely get the beer?**

and:

> **Should we consume the beer?**

---

# Stored Beer vs Immediate Consumption

The game should distinguish between:

## Beer Available

Beer exists in the world.

---

## Beer Collected

The team has acquired it.

---

## Beer Consumed

The Shooter actually drinks it.

This creates an important choice.

```text id="5x8a0n"
Collect Beer
    ↓
Store Beer
    ↓
Choose When to Drink
```

The team can save beer for:

* Bosses
* Dangerous encounters
* Build synergies
* Emergency power spikes

---

# Recommended Initial System

The simplest version should be:

```text id="f7a1xc"
Beer Pickup
    ↓
Beer Inventory Increases
    ↓
Player Presses Drink
    ↓
Intoxication Increases
    ↓
Benefits and Penalties Apply
```

Do not initially create a complicated inventory system.

The important thing to test is:

> **Is deciding when to drink fun?**

---

# Intoxication

Intoxication is the primary beer resource.

It should be represented as a percentage or meter.

Example:

```text id="s0gq3n"
0%
Sober
    ↓
25%
Tipsy
    ↓
50%
Drunk
    ↓
75%
Very Drunk
    ↓
100%
Wasted
```

The exact values can change.

The important thing is that intoxication should have recognizable stages.

---

# Intoxication Should Be Continuous

The system should ideally use a continuous value internally.

For example:

```text id="e9z4w2"
Intoxication = 0.0
        ↓
Intoxication = 0.25
        ↓
Intoxication = 0.50
        ↓
Intoxication = 0.75
        ↓
Intoxication = 1.00
```

Thresholds can then trigger special effects.

This gives designers more flexibility.

---

# Intoxication Thresholds

Each threshold should create a noticeable change.

## Sober

### Shooter

Normal combat.

### Rider

Normal handling.

---

## Tipsy

### Shooter

Small combat bonus.

### Rider

Slightly increased momentum.

The game should still feel mostly normal.

---

## Drunk

### Shooter

Significant combat bonus.

### Rider

Reduced traction or increased momentum.

The team begins to feel the consequences.

---

## Very Drunk

### Shooter

Major combat benefits.

### Rider

Handling becomes significantly more difficult.

The team must actively adapt.

---

## Wasted

### Shooter

Extremely powerful.

### Rider

The vehicle becomes difficult to control.

The team enters a high-risk state.

---

# Beer Benefits

Beer should provide meaningful benefits.

Possible benefits:

## Damage

The Shooter deals more damage.

---

## Attack Speed

The Shooter attacks faster.

---

## Projectile Effects

Beer may unlock:

* Explosions
* Piercing
* Chain reactions
* Homing

---

## Ability Power

Special abilities become stronger.

---

## Luck

Beer may increase the chance of:

* Critical hits
* Better drops
* Rare events

---

# Beer Penalties

The penalties should primarily affect control.

Possible effects:

## Increased Momentum

The cart takes longer to stop.

---

## Reduced Traction

The cart slides during turns.

---

## Delayed Steering

The cart reacts more slowly to input.

---

## Increased Turning

Small inputs create larger turns.

---

## Camera Sway

The camera moves unpredictably.

---

## Aim Sway

The Shooter has less precise aim.

---

# The Important Design Rule

The penalties should create:

> **More difficult decisions.**

They should not simply create:

> **Less fun.**

Bad:

> The player randomly loses control for five seconds.

Better:

> The cart has significantly more momentum and requires the Rider to plan braking earlier.

The player should be able to adapt.

---

# Rider Intoxication

The Rider should not necessarily become directly drunk.

The Shooter's intoxication can affect the cart.

This makes the relationship mechanically interesting.

For example:

```text id="0sxv48"
Shooter Drinks
    ↓
Shooter Gets Stronger
    ↓
Cart Handling Changes
```

The Rider must deal with the consequences of another player's decisions.

This is a powerful cooperative mechanic.

---

# Shooter Intoxication

The Shooter should directly benefit from drinking.

For example:

```text id="8j3r7z"
Intoxication
    ↓
Damage
    ↓
Attack Speed
    ↓
Special Effects
```

But the Shooter should also experience drawbacks.

Possible drawbacks:

* Aim sway
* Wider spread
* Delayed input
* Strange projectile behavior

The Shooter should be able to say:

> **I am more powerful, but less reliable.**

---

# Beer as a Build Axis

The team should be able to build around beer.

Possible build:

```text id="f9g8u5"
More Beer
    ↓
More Intoxication
    ↓
More Power
    ↓
Better High-Intoxication Handling
```

This creates a build where the team actively wants to become drunk.

---

# Beer Build Example

## Functional Alcoholic

### Upgrade 1

> Intoxication provides a small handling bonus.

### Upgrade 2

> High intoxication increases acceleration.

### Upgrade 3

> Intoxication reduces collision damage taken.

### Result

The team becomes more effective as intoxication increases.

This transforms the team's strategy from:

> **Avoid getting drunk.**

into:

> **Get drunk as quickly as possible.**

---

# Beer Synergy With Shooter Builds

## Drunken Machine Gun

```text id="f8o0r2"
High Intoxication
    +
High Fire Rate
    +
Multiple Projectiles
```

Result:

> Extremely high damage with increasingly chaotic accuracy.

---

## Drunken Berserker

```text id="8y9u7k"
High Intoxication
    +
Short-Range Weapon
    +
High Damage
```

Result:

> The Rider drives directly into enemies while the Shooter fires at close range.

---

## Drunken Crit Build

```text id="d0u2mx"
High Intoxication
    +
Critical Hits
    +
High Damage
```

Result:

> Huge damage spikes with unreliable precision.

---

# Beer Synergy With Rider Builds

## Drunk Driver

```text id="h8g3w1"
High Intoxication
    +
Improved Handling
```

The Rider becomes better at controlling the intoxicated cart.

---

## Alcoholic Rammer

```text id="v5l4b8"
High Intoxication
    +
High Speed
    +
Collision Damage
```

The team becomes a drunken projectile.

---

## Controlled Chaos

```text id="w7z3q6"
High Intoxication
    +
Drift
    +
Momentum Retention
```

The Rider learns to use unstable movement offensively.

---

# Beer Should Affect the Camera Carefully

Camera effects can communicate intoxication.

Possible effects:

* Gentle sway
* Delayed camera movement
* Slight roll
* FOV changes
* Camera bob

However:

> **The camera should never make the game physically uncomfortable.**

The player should understand:

> **The character is drunk.**

Without the player becoming genuinely uncomfortable.

The gameplay effects should come primarily from:

* Handling
* Aim
* Momentum

Not excessive screen distortion.

---

# Beer and Communication

Intoxication should create communication problems.

The Shooter may:

* Misjudge enemy distance
* Misidentify targets
* Overestimate their own damage
* Demand dangerous maneuvers

The Rider may need to decide:

> **Do I trust the drunk Shooter's plan?**

This can create natural comedy.

---

# Beer and Decision-Making

Beer should create decisions at multiple levels.

## Collection Decision

> **Can we safely get it?**

---

## Consumption Decision

> **Should we drink it now?**

---

## Build Decision

> **Should we invest in intoxication?**

---

## Crisis Decision

> **Should we drink more despite our current handling?**

---

# Beer as a Risk Escalation

The team should have a visible risk curve.

```text id="c0f3u1"
Low Intoxication
    ↓
Low Risk
    ↓
Moderate Power

Medium Intoxication
    ↓
Moderate Risk
    ↓
High Power

High Intoxication
    ↓
Extreme Risk
    ↓
Extreme Power
```

The team should decide where to stop.

Or deliberately refuse to stop.

---

# The "One More Beer" Mechanic

This should be a central psychological loop.

The team reaches a threshold.

The Shooter says:

> **"We should stop here."**

Then:

> **"Actually, one more beer would be really useful."**

Then:

> **"Okay, this is the last one."**

Then:

> **"Okay, now we're definitely done."**

The game should mechanically encourage this decision.

---

# Intoxication Threshold Rewards

Crossing a threshold could provide a temporary or permanent benefit.

Example:

```text id="t4w2a0"
Reach 25%
    ↓
Unlock Bonus

Reach 50%
    ↓
Unlock Stronger Bonus

Reach 75%
    ↓
Unlock Special Effect

Reach 100%
    ↓
Enter Maximum-Risk State
```

This makes reaching a threshold exciting.

---

# Going Beyond the Maximum

The game could potentially allow the team to exceed the normal intoxication limit.

For example:

```text id="x6k1s3"
100%
Wasted
    ↓
110%
Blackout
    ↓
120%
Absolutely Terrible Idea
```

This should be an optional high-risk strategy.

The team should be able to deliberately push beyond safe limits.

---

# Blackout State

A possible special state.

At extreme intoxication:

### Shooter

* Extremely powerful
* Highly inaccurate
* Special attacks unlocked

### Rider

* Extremely difficult handling
* Strong momentum
* Unusual vehicle behavior

The team may become:

> **Nearly unstoppable or completely doomed.**

This should be a high-risk build path.

---

# Beer and Temporary Effects

Not every beer needs to increase permanent intoxication.

Some beer pickups could provide temporary effects.

Examples:

## Strong Beer

Large intoxication increase.

---

## Light Beer

Small intoxication increase.

---

## Energy Beer

Temporary attack speed.

---

## Explosive Beer

Next attacks cause explosions.

---

## Mystery Beer

Random effect.

These should be introduced later.

The initial system should remain simple.

---

# Beer Quality

Different beer types can eventually create strategic choices.

Example:

| Beer Type    |    Power | Intoxication | Special Effect |
| ------------ | -------: | -----------: | -------------- |
| Light Beer   |      Low |          Low | None           |
| Normal Beer  |   Medium |       Medium | None           |
| Strong Beer  |     High |         High | None           |
| Energy Beer  |   Medium |       Medium | Attack Speed   |
| Mystery Beer | Variable |     Variable | Random         |

The exact values should be tuned through playtesting.

---

# Beer as a Reward Type

Beer should compete with other rewards.

The team may encounter:

```text id="5m5l7z"
Upgrade
    or
Beer
    or
Healing
```

This creates meaningful choices.

For example:

> **We could become stronger now, or we could drink and gain immediate power with long-term consequences.**

---

# Beer and Healing

Beer could potentially interact with health.

Possible designs:

## Beer Does Not Heal

This keeps the system focused.

---

## Beer Provides Temporary Protection

The Shooter gains a temporary shield.

---

## Beer Converts Health

The team sacrifices health for power.

This is much riskier.

The simplest initial version should probably keep beer separate from healing.

---

# Beer and the Run Structure

Beer availability should be controlled.

Too much beer:

> The team is always at maximum intoxication.

Too little beer:

> The mechanic becomes irrelevant.

The ideal situation is:

```text id="5h3x7r"
Beer Appears
    ↓
Team Wants It
    ↓
Team Can Reach It
    ↓
Team Must Decide Whether to Drink It
```

The team should frequently encounter beer without always being able to safely consume it.

---

# Beer Distribution

Beer can be distributed through:

## Normal Drops

Small amounts.

---

## Elite Rewards

Large amounts.

---

## Risky Locations

High amounts with dangerous access.

---

## Special Events

A major opportunity for intoxication.

---

# Beer and Enemy Design

Some enemies should specifically interact with beer.

Examples:

## Beer Thief

Steals beer from the battlefield.

---

## Drunk Enemy

Becomes stronger when near beer.

---

## Bouncer

Protects a large beer reward.

---

## Bartender Boss

Creates or throws beer across the battlefield.

These enemies make beer part of the battlefield rather than merely a number on the UI.

---

# Beer and Environmental Design

The environment can create beer-related situations.

Examples:

```text id="g1v5k9"
Beer Crate
    ↓
Surrounded by Enemies
```

The team must decide:

> **Is the beer worth the danger?**

Or:

```text id="5v5y3m"
Beer Located
    ↓
Far Away
```

The Rider must decide whether to travel toward it.

---

# The Beer Decision Matrix

The team should consider:

| Question                              | Relevant Factor      |
| ------------------------------------- | -------------------- |
| Can we reach it?                      | Rider control        |
| Is it worth getting?                  | Reward value         |
| Should we drink it?                   | Current intoxication |
| Can we handle more?                   | Current build        |
| Will it help against the next threat? | Upcoming encounter   |
| Can we afford the consequences?       | Team condition       |

This is the core beer decision system.

---

# Recommended Initial Implementation

The first prototype should only include:

```text id="5f8g2c"
Beer Drops
    ↓
Beer Inventory
    ↓
Drink Button
    ↓
Intoxication Meter
    ↓
Shooter Buffs
    ↓
Rider Handling Changes
```

Start with only three intoxication levels:

```text id="b3z0n5"
Sober
    ↓
Tipsy
    ↓
Drunk
```

Do not begin with:

* Ten beer types
* Complex alcohol chemistry
* Random blackout effects
* Large inventory systems
* Multiple temporary drink buffs

First test the core question:

> **Is becoming stronger while making the vehicle harder to control fun?**

---

# Initial Beer Prototype

A good first test could be:

## Every Beer

Provides:

```text
+10% Shooter Damage
```

And increases:

```text
+10% Cart Momentum
```

At thresholds:

```text
25% Intoxication
    ↓
Shooter Damage Bonus

50% Intoxication
    ↓
More Cart Momentum

75% Intoxication
    ↓
Shooter Accuracy Penalty

100% Intoxication
    ↓
Extreme Handling
```

These numbers are placeholders.

The important thing is to test the relationship.

---

# Beer Playtest Questions

### Power

* Does drinking beer feel immediately rewarding?
* Is the power increase noticeable?

### Risk

* Does intoxication create meaningful problems?
* Can the Rider adapt to it?

### Cooperation

* Does the Shooter want more beer than the Rider?
* Does this create interesting communication?

### Collection

* Is beer worth moving toward?
* Does collecting beer create spatial decisions?

### Build

* Can the team intentionally build around intoxication?
* Does a beer-focused build feel meaningfully different?

### Comedy

* Does the system naturally create funny moments?

---

# Beer Success Criteria

The beer system is successful if:

```text id="1k0m6f"
The Shooter wants to drink
        AND
The Rider fears the consequences
        AND
The team can adapt to intoxication
        AND
High intoxication creates new strategies
        AND
Beer affects movement and combat
        AND
The team makes meaningful decisions about consumption
```

---

# Final Beer Design Principle

Beer should not be:

> **A health potion with a funny animation.**

Beer should not be:

> **A simple damage buff with a movement debuff.**

Beer should be:

> **A decision that changes the way the entire team plays.**

The ideal progression is:

```text id="p7n5r2"
"Should we get the beer?"
        ↓
"Should we drink the beer?"
        ↓
"Can we handle the beer?"
        ↓
"Should we drink more?"
        ↓
"Why did we drink more?"
        ↓
"Drink another one."
```

The perfect beer mechanic creates a situation where the team is simultaneously:

> **More powerful than ever.**

and:

> **Less capable of controlling itself than ever.**

That tension should be one of the defining experiences of the game.

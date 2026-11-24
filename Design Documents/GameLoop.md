# Core Gameplay Loop

## Purpose

This document defines the moment-to-moment gameplay loop of the cooperative shopping cart roguelike.

The primary design goal is to make both player roles meaningful:

* The **Rider** controls positioning, momentum, and the cart itself.
* The **Shooter** controls combat and power growth.
* **Beer** makes the Shooter stronger while making the shared vehicle increasingly difficult to control.

The game should create a constant tension between:

> **Power vs. Control**

---

# Core Loop Summary

```text
Enter Arena
    ↓
Move Through Environment
    ↓
Find / Encounter Enemies
    ↓
Rider Positions the Cart
    ↓
Shooter Attacks Enemies
    ↓
Enemies Drop Rewards
    ↓
Players Choose Between Safety and Risk
    ↓
Collect Beer / Experience
    ↓
Shooter Becomes Stronger
    ↓
Intoxication Increases
    ↓
Cart Becomes More Difficult to Control
    ↓
Rider Adapts to New Handling
    ↓
Level Up
    ↓
Choose Upgrades
    ↓
Return to Combat
```

The loop should continuously escalate.

The players should become:

* More powerful
* More specialized
* More surrounded
* More intoxicated
* More difficult to control

---

# The Core Interaction

The central gameplay interaction is:

```text
Shooter kills enemies
        ↓
Beer becomes available
        ↓
Shooter drinks beer
        ↓
Shooter becomes stronger
        ↓
Vehicle becomes harder to control
        ↓
Rider must adapt
        ↓
The team can kill stronger enemies
        ↓
More beer becomes available
```

This creates a positive feedback loop.

The team is rewarded for taking risks, but the reward creates new problems.

---

# The Shared Vehicle

The cart is not merely transportation.

It is the shared space where the two players' decisions collide.

The cart should determine:

* Where the Shooter can attack from
* Which enemies can be reached
* Whether the team can escape
* Whether the Rider can use the cart offensively
* How difficult the Shooter's intoxication becomes to manage

The cart should be the game's central physical object.

---

# Rider Gameplay Loop

The Rider's gameplay loop should be:

```text
Observe Threats
    ↓
Choose a Position
    ↓
Manage Momentum
    ↓
Execute a Maneuver
    ↓
Create a Good Shooting Opportunity
    ↓
Escape / Attack / Reposition
    ↓
Repeat
```

The Rider should constantly make decisions about:

* Where to move
* How fast to move
* When to brake
* When to turn
* Whether to maintain momentum
* Whether to take a risk
* Whether to use the cart offensively

---

## Rider Decision Example

A group of enemies is approaching from the front.

The Rider can:

### Option A — Turn Away

* Safe
* Gives up nearby rewards
* May lose access to beer

### Option B — Ram Through

* Risky
* Can kill enemies
* May damage the cart

### Option C — Drift Around

* Requires skill
* Maintains momentum
* Keeps the Shooter in combat

### Option D — Brake

* Gives the Shooter a stable firing position
* Makes the cart vulnerable

### Option E — Boost

* Escapes quickly
* May overshoot the intended destination

The goal is for each option to have a meaningful advantage and disadvantage.

---

# Shooter Gameplay Loop

The Shooter's gameplay loop should be:

```text
Observe Enemies
    ↓
Aim
    ↓
Attack
    ↓
Kill Enemies
    ↓
Collect Rewards
    ↓
Choose Targets
    ↓
Choose When to Drink
    ↓
Choose Upgrades
    ↓
Become Stronger
    ↓
Repeat
```

The Shooter should constantly make decisions about:

* Which enemy to target
* Whether to prioritize dangerous enemies or reward-bearing enemies
* Whether to collect beer immediately
* Whether to drink beer now or save it
* Whether to pursue a more powerful build
* Whether the Rider is currently in a position to support the decision

---

# The Shared Decision Loop

The strongest part of the game should come from the fact that neither player has complete control over the situation.

```text
Shooter wants power
        ↓
Shooter drinks beer
        ↓
Intoxication increases
        ↓
Rider loses control
        ↓
Rider takes greater risks
        ↓
Shooter gets better opportunities
        ↓
More enemies are killed
        ↓
More beer is found
```

This should create situations where the team is simultaneously:

* Stronger
* Faster
* More powerful
* Less coordinated
* More difficult to control

---

# Beer Loop

Beer should be a meaningful decision rather than an automatic pickup.

The basic interaction:

```text
Beer Found
    ↓
Collect Beer
    ↓
Choose When to Drink
    ↓
Gain Power
    ↓
Gain Intoxication
    ↓
Accept New Control Problems
```

Potentially, beer should not immediately be consumed upon pickup.

The Shooter may carry beer and decide when to drink it.

This creates an additional decision:

> **Do we drink now, or save it for a more dangerous situation?**

---

# Intoxication Loop

Intoxication should affect the game gradually.

Example:

```text
SOBER
    ↓
TIPSY
    ↓
DRUNK
    ↓
WASTED
```

Each stage should provide benefits and penalties.

## Sober

### Benefits

* Reliable controls
* Normal aiming
* Predictable movement

### Drawback

* No intoxication bonuses

---

## Tipsy

### Benefits

* Small combat bonus
* Slightly stronger abilities

### Drawbacks

* Minor control changes
* Mild camera effects

---

## Drunk

### Benefits

* Significant combat bonuses
* Faster attacks
* Stronger abilities

### Drawbacks

* Increased cart momentum
* More difficult aiming
* Reduced precision

---

## Wasted

### Benefits

* Extremely powerful combat abilities
* Potentially unique effects

### Drawbacks

* Very difficult control
* Exaggerated momentum
* Major aiming challenges

The system should ideally create a situation where:

> **Being drunk is desirable, but being too drunk is dangerous.**

---

# Intoxication Should Change Physics

The preferred design direction is to make intoxication affect the physical behavior of the cart rather than simply applying random effects.

Examples:

### Increased Momentum

The cart takes longer to stop.

### Reduced Traction

The cart slides more during turns.

### Exaggerated Turning

Small inputs create larger rotations.

### Delayed Response

The cart reacts slightly slower to steering.

### Increased Speed

The cart accelerates more aggressively.

These effects create challenges that the Rider can learn to adapt to.

Avoid relying primarily on:

> "The game randomly takes control away from the player."

The goal is to create **difficult but learnable handling**.

---

# Combat Positioning Loop

The Rider and Shooter should constantly interact through positioning.

```text
Rider moves
    ↓
Shooter gains or loses line of sight
    ↓
Shooter attacks
    ↓
Enemies react
    ↓
Rider changes position
    ↓
Shooter adjusts target
```

The Rider should be able to help the Shooter by:

* Turning toward enemies
* Creating a clear firing angle
* Maintaining distance
* Approaching valuable targets
* Avoiding obstacles

The Shooter should help the Rider by:

* Killing enemies blocking escape routes
* Removing dangerous enemies
* Protecting the cart
* Controlling areas around the vehicle

Neither player should be entirely independent.

---

# The Cart as a Weapon

The Rider should have reasons to intentionally approach danger.

Possible cart combat loop:

```text
Build Momentum
    ↓
Choose Target
    ↓
Approach Enemy
    ↓
Ram
    ↓
Deal Damage
    ↓
Escape Before Being Surrounded
```

This gives the Rider an offensive gameplay loop independent from shooting.

Potential cart damage factors:

```text
Collision Damage =
Speed
×
Cart Upgrade
×
Impact Type
```

Possible upgrades:

* Spikes
* Reinforced front
* Explosive collision
* Knockback
* Piercing impact
* Shockwave
* Increased collision damage at high speed

---

# Combat Encounter Structure

The game should not require the team to fight every enemy.

The team should constantly choose between:

```text
Fight
    or
Escape
```

Possible encounter decisions:

### Fight

* Gain experience
* Gain beer
* Risk taking damage
* Increase intoxication

### Escape

* Preserve health
* Avoid dangerous enemies
* Lose potential rewards

### Aggressive Positioning

* Approach a dangerous group
* Attempt to quickly eliminate them
* Gain valuable rewards

### Defensive Positioning

* Maintain distance
* Fight safely
* Sacrifice efficiency for survival

This makes the Rider's movement decisions meaningful.

---

# Level-Up Loop

The basic progression loop should be:

```text
Kill Enemies
    ↓
Gain Experience
    ↓
Level Up
    ↓
Present Upgrade Choices
    ↓
Shooter or Rider Chooses
    ↓
Build Becomes Stronger
    ↓
Enemy Difficulty Increases
```

The upgrade system should eventually support two separate build paths.

---

# Shooter Progression

Example:

```text
Basic Weapon
    ↓
More Damage
    ↓
More Projectiles
    ↓
More Attack Speed
    ↓
Special Effects
    ↓
Build Identity
```

Possible build directions:

* Projectile swarm
* High-damage sniper
* Explosive weapons
* Elemental effects
* Homing attacks
* Beer-based abilities

---

# Rider Progression

Example:

```text
Basic Cart
    ↓
Better Handling
    ↓
Better Mobility
    ↓
Better Collision Damage
    ↓
Special Vehicle Abilities
    ↓
Vehicle Build Identity
```

Possible build directions:

* Speed
* Drifting
* Ramming
* Defense
* Mobility
* Crowd control

---

# The Two Builds Should Interact

The Shooter and Rider should not be completely separate.

Some upgrades should create synergies.

## Example: Speed Shooter

### Shooter

* More damage while moving quickly

### Rider

* Higher maximum speed

Result:

> The Rider constantly tries to maintain high speed while the Shooter benefits from it.

---

## Example: Ram Build

### Rider

* High collision damage

### Shooter

* Gains bonuses when enemies are hit by the cart

Result:

> Both players want to aggressively drive into enemies.

---

## Example: Drunkenness Build

### Shooter

* Stronger while intoxicated

### Rider

* Improved handling while intoxicated

Result:

> The Rider actively wants the Shooter to drink more.

This creates cooperative build synergies.

---

# Reward Loop

Rewards should create choices rather than simply increase numbers.

Possible rewards:

* Experience
* Beer
* Temporary powerups
* Upgrade choices
* Currency
* Rare items

The ideal reward sequence is:

```text
Risk
    ↓
Reward
    ↓
Decision
    ↓
Build Change
    ↓
New Strategy
```

---

# Enemy Escalation

The game should gradually increase pressure.

Possible escalation:

```text
More Enemies
    ↓
Stronger Enemies
    ↓
More Enemy Types
    ↓
More Environmental Threats
    ↓
Elite Enemies
    ↓
Boss Encounter
```

The team should become more powerful while the environment becomes more dangerous.

---

# Example Ten-Minute Run

## Minute 0–2: Sober Start

The team begins with:

* Basic cart
* Basic weapon
* Normal handling

The Rider learns the arena.

The Shooter kills weak enemies.

The team collects their first beer.

---

## Minute 2–4: First Risk

The Shooter drinks.

The Shooter becomes stronger.

The cart begins to handle differently.

The Rider adapts to:

* Increased momentum
* Reduced traction
* More aggressive movement

The team begins taking more risks.

---

## Minute 4–6: Build Identity

The team has selected several upgrades.

The build begins to specialize.

Examples:

* Fast cart + high fire rate
* Ram cart + shotgun
* Drifting cart + explosive weapon

Enemies become more numerous.

---

## Minute 6–8: Escalation

The team is now powerful but less reliable.

The Shooter wants more beer.

The Rider is struggling to maintain control.

The team must choose between:

* Fighting for more rewards
* Escaping to survive

---

## Minute 8–10: Controlled Chaos

The team is now highly specialized.

The cart is difficult to control.

The Shooter is extremely powerful.

The arena is full of enemies.

The team must use their build synergy to survive.

The run ends with:

* Survival
* Death
* A boss encounter
* A final objective

---

# The Core Tension

The entire game should repeatedly return to this relationship:

```text
More Power
    ↓
More Risk
    ↓
Less Control
    ↓
More Skill Required
    ↓
More Reward
```

The player should never feel that the game is simply making them weaker.

Instead:

> **The player becomes more powerful, but the challenge changes from "Can we kill the enemies?" to "Can we control ourselves while killing the enemies?"**

---

# The Five-Second Test

During development, evaluate the Rider's gameplay by asking:

> **Does the Rider have an interesting decision to make every few seconds?**

Possible decisions:

* Turn
* Brake
* Drift
* Boost
* Ram
* Escape
* Reposition
* Chase a reward
* Maintain momentum
* Protect the Shooter

If the answer is consistently no, the Rider role needs more mechanics.

---

# The Ten-Minute Test

The first playable prototype should answer:

> **Can two players enjoy the core loop for ten minutes without needing permanent progression?**

The prototype should contain only enough systems to test:

```text
Drive
    ↓
Fight
    ↓
Collect
    ↓
Drink
    ↓
Become Stronger
    ↓
Become Harder to Control
    ↓
Adapt
    ↓
Repeat
```

If this loop works, the larger roguelike progression system has a strong foundation.

---

# Core Design Principle

The game should not be built around:

> **"A survivor-like game with two players."**

It should be built around:

> **"Two players sharing one increasingly powerful and increasingly difficult-to-control vehicle."**

The shooter and rider should both be necessary.

The shooter should make the team stronger.

The rider should make the team effective.

Beer should make the team more powerful while making cooperation more difficult.

That interaction is the core of the game.

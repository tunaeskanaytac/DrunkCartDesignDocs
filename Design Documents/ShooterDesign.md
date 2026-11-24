# Shooter Design

## Purpose

The Shooter is responsible for the team's offensive power.

The Shooter should:

* Aim
* Attack enemies
* Choose targets
* Collect rewards
* Manage beer
* Build a combat identity
* Support the Rider during dangerous maneuvers

The Shooter's role should not be:

> **Stand in the cart and shoot everything.**

The Shooter should constantly make decisions about:

> **What to shoot, when to shoot it, where to aim, and how much power is worth the risk of becoming more intoxicated.**

---

# The Shooter's Core Fantasy

The Shooter is:

> **A heavily armed passenger who becomes increasingly powerful and increasingly drunk while the Rider desperately tries to keep the vehicle under control.**

The Shooter should feel like the team's source of escalating power.

The Rider creates opportunities.

The Shooter converts those opportunities into:

* Kills
* Experience
* Beer
* Power

---

# Shooter Gameplay Loop

```text id="0g1n7v"
Observe Battlefield
    ↓
Choose Target
    ↓
Aim
    ↓
Attack
    ↓
Kill Enemies
    ↓
Collect Rewards
    ↓
Choose Whether to Drink
    ↓
Gain Power
    ↓
Choose Upgrades
    ↓
Support the Rider
    ↓
Repeat
```

The Shooter's loop should be active even when the Rider is moving quickly.

---

# The Shooter's Main Decisions

The Shooter should constantly decide:

## Which Enemy to Attack?

Potential priorities:

* Closest enemy
* Most dangerous enemy
* Weakest enemy
* Enemy carrying a reward
* Enemy blocking an escape route
* Enemy threatening the Rider

---

## Where to Aim?

The Rider's movement should affect the Shooter's firing position.

The Shooter may need to:

* Lead moving targets
* Aim around the cart
* Fire behind the vehicle
* Shoot while drifting
* Adjust for vehicle movement

---

## When to Drink?

The Shooter should decide:

```text id="g3xq2k"
Drink Now
    or
Save Beer
```

Drinking immediately:

* Increases power
* Increases intoxication
* Makes future combat easier

Saving beer:

* Preserves control
* Allows a stronger future power spike
* May be useful before a difficult encounter

---

# The Shooter Should Have a Real Weapon

The initial weapon should be simple but satisfying.

The first weapon should establish:

* Fire rate
* Projectile behavior
* Damage
* Range
* Accuracy
* Impact feedback

The weapon should feel good before upgrades are added.

---

# Recommended Initial Weapon

A simple ranged weapon is the best starting point.

Possible examples:

* Pistol
* Water gun
* Crossbow
* Slingshot
* Bottle launcher
* Improvised weapon

The exact weapon can change later.

The important thing is:

> **The Shooter should have a clear target and a satisfying attack.**

---

# Aiming While Moving

The Shooter should have to aim while the cart is moving.

This creates a direct connection between both players.

The Rider controls:

```text id="wqg8ks"
Position
    ↓
Velocity
    ↓
Orientation
```

The Shooter controls:

```text id="4q6zqj"
Aim Direction
    ↓
Target Selection
    ↓
Attack Timing
```

The two systems interact continuously.

Rider's moving style should make an impact on Shooter's aim otherwise the shooter mechanics would be too easy and this concludes as a not fun gameplay. Currently there are two possible solutions for this problem:
	One would be to set the Shooter's aim relevant to the Cart's direction. Which would cause problems if the aim by mouse is set to instant snap so mouse aiming would require delay. ![[Pasted image 20260728203736.png]]
	Other would be to use only trajectory-based aiming system so that the aiming would require skill at all times. ![[Pasted image 20260728204634.png]]
	But this solution isn't preferred because we would like to introduce various shooting mechanics for the shooter and this approach limits us to only one.
	*These aproaches are open to discussion and new ideas are welcome.*
	^ShooterAimingMechanicProblem

---

# Vehicle Movement Should Affect Shooting

The Shooter should not feel as though they are standing on a stationary platform.

Possible effects:

* Cart momentum affects aim
* Sharp turns require aim correction
* Drifting changes the firing angle
* Boosting creates a short aiming challenge
* Intoxication makes aiming more difficult

The Shooter should feel:

> **I am firing from a moving vehicle.**

---

# Shooter Positioning

The Shooter's position in the cart should matter.

The Shooter may have:

* A fixed seat
* A rotating upper body
* A limited firing arc
* A turret-like aiming system

The simplest initial version is:

> **The Shooter can aim freely while the Rider controls the cart.**

More restrictive positioning can be added later if needed.

---

# The Shooter's Relationship with the Rider

The Shooter should depend on the Rider for:

* Position
* Range
* Line of sight
* Escape
* Access to rewards

The Rider should depend on the Shooter for:

* Clearing enemies
* Removing threats
* Creating safe paths
* Defending the cart

This creates a two-way dependency.

---

# Combat Positioning

The Shooter should constantly communicate with the Rider.

Examples:

> "Move closer."

> "Turn around."

> "There's a big enemy behind us."

> "Get me toward that beer."

> "I can't shoot from here."

> "Keep moving!"

The Shooter should have opinions about where the cart goes.

However, the Rider should remain the person who actually controls the vehicle.

---

# Target Priority

The Shooter should have meaningful target decisions.

Possible target categories:

## Immediate Threat

Enemies currently attacking the cart.

---

## High-Value Enemy

Enemies with:

* More experience
* Better rewards
* Rare beer
* Special effects

---

## Escape Threat

Enemies that block the team's escape path.

---

## Opportunity Target

Enemies that can be killed quickly for rewards.

---

The Shooter should sometimes have to choose:

> **Do I kill the enemy attacking us, or do I chase the valuable target?**

---

# Shooter Combat Builds

The Shooter should eventually be able to specialize.

## Projectile Build

Focus:

* More projectiles
* Wider spread
* Pierce
* Projectile size

Gameplay:

> **Cover the battlefield with bullets.**

---

## Fire Rate Build

Focus:

* Attack speed
* Reload speed
* Cooldown reduction

Gameplay:

> **Constant pressure.**

---

## Critical Hit Build

Focus:

* High single-target damage
* Critical hits
* Weak-point damage

Gameplay:

> **Prioritize important targets.**

---

## Explosive Build

Focus:

* Area damage
* Chain reactions
* Enemy groups

Gameplay:

> **Shoot one enemy to destroy many.**

---

## Homing Build

Focus:

* Tracking projectiles
* Target prioritization
* Reduced aiming requirements

Gameplay:

> **Focus on movement and target selection.**

---

## Beer Build

Focus:

* Intoxication
* Beer generation
* Power scaling based on drunkenness

Gameplay:

> **Become stronger by becoming more drunk.**

---

# Beer as the Shooter's Core Resource

Beer should be more than a passive reward.

The Shooter should actively make decisions about it.

Possible states:

```text id="y10qwp"
Beer Available
    ↓
Collect Beer
    ↓
Store Beer
    ↓
Choose Timing
    ↓
Drink
    ↓
Increase Intoxication
    ↓
Gain Power
```

This creates a decision:

> **Is the current situation worth becoming more intoxicated?**

---

# Beer Should Create a Power Curve

The Shooter's power can increase with intoxication.

Example:

```text id="r6b2gc"
Intoxication
    ↓
Damage
    ↓
Attack Speed
    ↓
Special Effects
```

But the Rider's control challenge also increases.

This creates:

```text id="y3l0g3"
More Beer
    ↓
More Shooter Power
    ↓
More Intoxication
    ↓
More Vehicle Difficulty
```

---

# Intoxication Effects on the Shooter

The Shooter should gain meaningful combat benefits.

Possible effects:

## Tipsy

* +10% damage

---

## Drunk

* +25% damage
* +15% attack speed

---

## Wasted

* Major damage bonus
* Special weapon effects

---

The benefits should be significant enough that the Shooter genuinely wants to become drunk.

---

# Intoxication Effects on Aiming

Intoxication can also affect the Shooter directly.

Possible effects:

* Increased aim sway
* Delayed aim response
* Wider projectile spread
* Reduced precision
* Unusual projectile behavior

However, these effects should not make the Shooter feel useless.

The goal is:

> **More power, less precision.**

This creates a natural tradeoff.

---

# The Shooter's Skill Ceiling

The Shooter's skill should come from:

## Target Selection

Choosing the right enemy.

---

## Aim

Hitting targets accurately.

---

## Timing

Knowing when to attack and when to wait.

---

## Position Awareness

Understanding the cart's movement.

---

## Risk Management

Knowing when beer is worth the consequences.

---

# The Shooter Should Help the Rider

The Shooter is not simply a damage dealer.

The Shooter should actively support the Rider.

Possible responsibilities:

* Kill enemies blocking escape routes
* Eliminate enemies approaching from the side
* Protect the cart during a maneuver
* Kill high-priority targets
* Clear a path before the Rider rams

The Shooter should sometimes think:

> **I don't need to kill the strongest enemy. I need to kill the enemy preventing us from escaping.**

---

# Combat and Vehicle Synergy

The Shooter's upgrades should sometimes interact with vehicle movement.

Examples:

## Momentum Shot

> Deal increased damage based on the cart's current speed.

This encourages the Rider to maintain momentum.

---

## Drift Fire

> Gain increased attack speed while the cart is drifting.

This encourages coordinated maneuvers.

---

## Impact Mark

> Enemies hit by the cart take increased damage from the Shooter.

This creates:

```text id="t6c2ci"
Rider Rams
    ↓
Enemy Becomes Vulnerable
    ↓
Shooter Finishes Enemy
```

---

## Protective Fire

> Killing enemies near the cart temporarily reduces incoming damage.

This rewards the Shooter for protecting the vehicle.

---

# Shooter Upgrade Philosophy

Shooter upgrades should not only increase numbers.

They should change:

* Targeting
* Range
* Attack patterns
* Movement interaction
* Beer interaction
* Team synergy

A good upgrade should create a new decision.

---

# Example Shooter Upgrades

## Double Shot

Fire an additional projectile.

---

## Piercing Rounds

Projectiles pass through enemies.

---

## Drunken Fury

Damage increases with intoxication.

---

## Last Call

When intoxication reaches a high level, gain a temporary damage burst.

---

## Steady Hands

Reduce the negative effects of intoxication on aiming.

---

## Reckless Drinking

Beer provides more power but increases intoxication faster.

---

## Momentum Shot

Deal more damage while the cart is moving quickly.

---

## Drive-By

Gain increased fire rate while the cart is moving.

---

## Covering Fire

Killing enemies near the cart grants temporary protection.

---

## Cart Mark

Enemies hit by the cart take increased damage from the Shooter.

---

# The Shooter's Build Should Affect the Rider

This is important.

The Shooter's build should sometimes change how the Rider wants to drive.

Examples:

### High-Speed Build

The Shooter benefits from high vehicle speed.

The Rider wants to maintain momentum.

---

### Precision Build

The Shooter benefits from stable positioning.

The Rider wants to avoid sudden turns.

---

### Close-Range Build

The Shooter must get close to enemies.

The Rider must drive aggressively.

---

### Area-Damage Build

The Shooter wants to be surrounded by enemies.

The Rider must control enemy grouping.

---

### Beer Build

The Shooter wants high intoxication.

The Rider must learn to handle difficult physics.

---

# Shooter Build Archetypes

## The Machine Gun Drunk

### Focus

* Fire rate
* Intoxication
* Projectile count

### Gameplay

The Shooter becomes increasingly powerful and increasingly inaccurate.

The Rider must survive the resulting chaos.

---

## The Sniper

### Focus

* Damage
* Critical hits
* Precision

### Gameplay

The Rider positions the cart carefully while the Shooter eliminates high-priority enemies.

---

## The Brawler

### Focus

* Short range
* Area damage
* Knockback

### Gameplay

The Rider drives directly into enemy groups.

---

## The Beer Wizard

### Focus

* Intoxication
* Beer generation
* Special effects

### Gameplay

The Shooter's abilities become increasingly strange as they drink.

---

## The Support Shooter

### Focus

* Defensive fire
* Crowd control
* Protection

### Gameplay

The Shooter prioritizes keeping the cart safe rather than maximizing kills.

---

# Shooter and Rider Communication

The Shooter should have reasons to communicate:

> "Left!"

> "Slow down!"

> "Keep going!"

> "There's beer!"

> "Big enemy!"

> "I need a better angle!"

> "Don't drink that!"

The Rider should also communicate:

> "I'm turning!"

> "I'm boosting!"

> "I can't stop!"

> "We're going for it!"

The goal is not to force communication.

The goal is to create situations where communication naturally improves performance.

---

# The Shooter's Position in the Team

The Shooter is responsible for:

```text id="9r0r6s"
Threat Removal
    +
Target Selection
    +
Power Growth
    +
Reward Generation
    +
Team Protection
```

The Rider is responsible for:

```text id="i0o7ab"
Position
    +
Momentum
    +
Escape
    +
Collision
    +
Team Movement
```

Together:

```text id="ghm4lb"
Rider Creates Opportunity
        ↓
Shooter Converts Opportunity into Power
        ↓
Power Creates More Rewards
        ↓
Rewards Create More Risk
        ↓
Rider Must Adapt
```

---

# Prototype Version of the Shooter

The first version should contain:

```text id="7j3jqn"
One Weapon
    +
Aiming
    +
Shooting
    +
One Enemy Type
    +
Beer Drops
    +
Drinking
    +
Intoxication
    +
Three Upgrade Choices
```

This is enough to validate the Shooter role.

---

# Recommended Initial Shooter Weapon

The first weapon should be:

* Easy to understand
* Satisfying to fire
* Effective at medium range
* Simple to upgrade

The exact weapon can be changed later.

The important thing is to test:

> **Does shooting from a moving shopping cart feel good?**

---

# Shooter Playtest Questions

### Combat

* Is shooting satisfying?
* Do enemies feel good to hit?
* Are targets easy to understand?
* Does aiming while moving feel interesting?

### Positioning

* Does the Rider's movement affect combat?
* Does the Shooter care where the cart is?
* Can the Shooter communicate useful positioning information?

### Beer

* Does the Shooter want to drink?
* Is the power increase noticeable?
* Is the risk worth the reward?

### Progression

* Do upgrades change the way the Shooter plays?
* Do different builds feel distinct?
* Do upgrades affect the Rider's decisions?

### Cooperation

* Does the Shooter need the Rider?
* Does the Rider need the Shooter?
* Do the two players naturally coordinate?

---

# Shooter Success Criteria

The Shooter role is successful if:

```text id="x9c4ax"
Shooting feels satisfying
        AND
Target selection matters
        AND
Vehicle movement affects combat
        AND
Beer creates meaningful risk
        AND
Upgrades create distinct builds
        AND
The Shooter supports the Rider
```

---

# Final Design Principle

The Shooter should not be:

> **A normal survivor-like character sitting in a shopping cart.**

The Shooter should be:

> **The team's source of escalating power, whose decisions directly make the shared vehicle more difficult to control.**

The Rider controls:

> **Where the team is.**

The Shooter controls:

> **What the team can kill.**

Beer controls:

> **How powerful and how chaotic the team becomes.**

---

# Core Shooter Fantasy

The ideal Shooter experience is:

```text id="v9z1d3"
"I can handle this."
    ↓
"Give me that beer."
    ↓
"Look at my damage!"
    ↓
"Why is my aim doing that?"
    ↓
"MORE BEER."
    ↓
"WHY ARE WE TURNING?"
    ↓
"SHOOT THE BIG ONE!"
    ↓
"WHICH BIG ONE?"
    ↓
"ALL OF THEM!"
```

The Shooter should create the combat chaos.

The Rider should create the physical chaos.

The game should emerge from both systems escalating together.

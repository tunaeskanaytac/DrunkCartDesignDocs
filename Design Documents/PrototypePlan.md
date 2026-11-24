# Prototype Plan

## Purpose

This document defines the development plan for the first playable prototype.

The goal is not to create a complete game.

The goal is to answer one question:

> **Is it fun for two players to share a shopping cart while one player fights and becomes stronger, and the other player tries to control the increasingly difficult vehicle?**

The prototype should be built around validating this core interaction as quickly as possible.

---

# Prototype Scope

The first prototype should contain:

* One arena
* One shopping cart
* One Rider
* One Shooter
* One basic weapon
* One basic enemy
* Beer pickups
* Intoxication
* Basic vehicle handling
* Basic shooting
* A simple level-up system
* A small number of upgrades
* A simple survival objective

The prototype does **not** need:

* Multiple maps
* Permanent progression
* Complex menus
* Story
* Extensive character customization
* Many weapons
* Many enemy types
* Advanced visual effects
* Final art
* Online multiplayer

---

# Development Philosophy

Build in this order:

```text id="8d2o4b"
Physical Interaction
    ↓
Combat
    ↓
Rewards
    ↓
Intoxication
    ↓
Progression
    ↓
Escalation
    ↓
Polish
```

Do not build systems that depend on the core loop being fun before validating the core loop.

---

# Phase 0 — Define the Test

Before implementing anything, define the prototype's success criteria.

The prototype succeeds if:

### Rider

* Driving is enjoyable
* Momentum creates meaningful decisions
* The Rider can avoid enemies through skill
* The cart can be used offensively
* Intoxication creates a new handling challenge rather than simply taking control away

### Shooter

* Shooting feels satisfying
* The Shooter has meaningful targets
* Beer creates a desirable risk/reward decision
* The Shooter has meaningful upgrade choices

### Team

* The players need each other
* The Rider's positioning affects the Shooter
* The Shooter's power affects the Rider
* The two players naturally communicate

The most important test is:

> **Would the players want to play another run?**

---

# Phase 1 — Build the Cart

## Goal

Make driving enjoyable before adding enemies or progression.

The first scene should contain:

* A flat arena
* A shopping cart
* A Rider controller
* Camera
* Basic obstacles

No combat is required yet.

---

## Basic Cart Movement

The cart should have:

* Acceleration
* Maximum speed
* Braking
* Turning
* Momentum

Avoid making the cart behave like a character controller.

The Rider should feel like they are controlling a vehicle.

A basic movement model:

```text id="f5g0nq"
Input
    ↓
Acceleration
    ↓
Velocity
    ↓
Momentum
    ↓
Steering
    ↓
Vehicle Movement
```

---

## Initial Driving Test

Create a simple obstacle course.

The Rider should be able to:

* Accelerate
* Brake
* Turn
* Avoid obstacles
* Maintain momentum
* Perform sharp turns

The first question is:

> **Is controlling the cart fun when there is nothing else to do?**

If the answer is no, do not proceed to progression.

---

# Phase 2 — Add Vehicle Skill

Once basic driving works, add one or two advanced mechanics.

Recommended first mechanics:

## Drift

Allows the cart to turn while maintaining speed.

## Boost

Provides a short burst of acceleration.

Do not add every possible mechanic immediately.

The goal is to test whether the Rider has a skill ceiling.

---

# Phase 3 — Add Cart Combat

Give the Rider a reason to interact with enemies.

Start with one simple attack:

> **Ram**

The cart damages enemies based on collision speed.

Example:

```text id="3w2nbi"
Speed
    ×
Collision Modifier
    =
Impact Damage
```

The Rider should be able to:

```text
Build Speed
    ↓
Choose Enemy
    ↓
Ram
    ↓
Deal Damage
    ↓
Escape
```

This creates a basic vehicle combat loop.

---

# Phase 4 — Add the Shooter

Add a second player to the cart.

The Shooter should initially have:

* One weapon
* Aiming
* Shooting
* Ammunition or cooldown
* Basic targeting

The Shooter should be able to attack independently of the Rider.

The two players should now have separate responsibilities:

```text
Rider:
Position the cart

Shooter:
Attack enemies
```

---

# Phase 5 — Test Positioning

Before adding progression, test whether the two roles interact properly.

Create enemies that force the Rider to move.

Examples:

### Chaser

Approaches the cart.

### Ranged Enemy

Attacks from a distance.

The Rider must now decide:

* Stay close enough for the Shooter to attack
* Keep distance from enemies
* Position the Shooter toward targets
* Avoid being surrounded

The Shooter must:

* Aim while moving
* Prioritize targets
* Communicate with the Rider

This phase should answer:

> **Does the Rider's movement meaningfully affect the Shooter's gameplay?**

---

# Phase 6 — Add Beer

Introduce the game's main risk/reward mechanic.

The first implementation should be extremely simple.

```text
Enemy Dies
    ↓
Beer Drops
    ↓
Shooter Collects Beer
    ↓
Shooter Drinks Beer
    ↓
Power Increases
    ↓
Handling Difficulty Increases
```

Do not initially implement multiple beer types.

Start with one beer resource.

---

# Phase 7 — Add Intoxication

Create a simple intoxication value.

For example:

```text id="9u7glh"
0% ─────────────── 100%
Sober             Wasted
```

The intoxication value should affect:

* Shooter power
* Cart handling

Possible effects:

### Low Intoxication

* Slight damage bonus
* Minor handling changes

### Medium Intoxication

* Significant combat bonus
* More momentum
* Reduced traction

### High Intoxication

* Major combat bonus
* Difficult handling
* Strong movement consequences

The first version should use predictable effects.

For example:

```text
Intoxication increases
        ↓
Acceleration increases
        ↓
Braking becomes weaker
        ↓
Turning becomes more difficult
```

This gives the Rider a challenge they can learn.

---

# Phase 8 — Add Experience and Leveling

Once the base loop works, add progression.

The basic loop:

```text
Kill Enemies
    ↓
Gain Experience
    ↓
Level Up
    ↓
Choose Upgrade
    ↓
Become Stronger
```

Initially, use a simple upgrade screen.

For example:

```text
LEVEL UP

[ +20% Damage ]

[ +10% Cart Acceleration ]

[ Beer lasts longer ]
```

The goal is not to create a complete build system yet.

The goal is to test whether upgrades make the run more interesting.

---

# Phase 9 — Separate Upgrade Pools

Once basic level-ups work, separate upgrades into categories.

## Shooter Upgrades

Examples:

* Damage
* Fire rate
* Projectile count
* Projectile size
* Pierce
* Explosions

## Rider Upgrades

Examples:

* Acceleration
* Maximum speed
* Turning
* Braking
* Drift
* Collision damage
* Armor

## Shared Upgrades

Examples:

* Beer efficiency
* Intoxication resistance
* Experience gain
* Shared health
* Reward collection range

---

# Phase 10 — Test Build Synergy

Add a small number of upgrades that encourage cooperation.

Example:

## Speed Build

### Rider

Higher maximum speed.

### Shooter

More damage while moving quickly.

---

## Ram Build

### Rider

More collision damage.

### Shooter

Bonus damage against enemies recently hit by the cart.

---

## Drunkenness Build

### Shooter

More power at higher intoxication.

### Rider

Improved handling while the Shooter is intoxicated.

The goal is to create builds where:

> **The best outcome for one player is also useful to the other player.**

---

# Phase 11 — Add Enemy Escalation

Once the core loop works, gradually increase pressure.

Start with:

```text
More Enemies
```

Then add:

```text
Stronger Enemies
```

Then:

```text
New Enemy Behaviors
```

Then:

```text
Elite Enemies
```

Finally:

```text
Bosses
```

Do not add many enemy types before knowing what the core combat loop requires.

---

# Suggested Prototype Enemy Roster

## Enemy 1 — Chaser

Purpose:

* Tests movement
* Forces the Rider to reposition

Behavior:

```text
Find Cart
    ↓
Move Toward Cart
    ↓
Attack When Close
```

---

## Enemy 2 — Ranged Enemy

Purpose:

* Tests positioning
* Forces the team to avoid staying still

Behavior:

```text
Maintain Distance
    ↓
Attack Cart
    ↓
Reposition
```

---

## Enemy 3 — Heavy Enemy

Purpose:

* Creates a dangerous target
* Tests whether the team chooses to fight or flee

Behavior:

```text
Slow Movement
    ↓
High Health
    ↓
High Damage
```

---

# Phase 12 — Create a Ten-Minute Run

Once the systems work independently, combine them.

The first complete run should be approximately:

> **10 minutes**

The run should include:

```text
Start
    ↓
Basic Combat
    ↓
First Beer
    ↓
First Intoxication
    ↓
First Level Up
    ↓
Build Development
    ↓
Enemy Escalation
    ↓
Increasing Control Difficulty
    ↓
Final Challenge
```

The run should have a clear ending.

Possible endings:

* Survive for ten minutes
* Defeat a boss
* Reach an extraction point
* Complete a final objective

For the first prototype, a timer is probably the simplest.

---

# Prototype Development Order

Recommended order:

```text
1. Cart Movement
        ↓
2. Cart Momentum
        ↓
3. Cart Combat
        ↓
4. Shooter Combat
        ↓
5. Enemy AI
        ↓
6. Player Positioning
        ↓
7. Beer Pickup
        ↓
8. Intoxication
        ↓
9. Experience
        ↓
10. Level-Up Choices
        ↓
11. Upgrades
        ↓
12. Enemy Escalation
        ↓
13. Ten-Minute Run
        ↓
14. Polish
```

---

# What Not to Build Yet

Avoid spending time on:

## Permanent Meta-Progression

First determine whether a single run is fun.

---

## Many Characters

One Rider and one Shooter are enough.

---

## Many Weapons

One weapon is enough to validate the combat loop.

---

## Large Maps

One arena is enough.

---

## Complex Inventory Systems

Beer can be a simple resource initially.

---

## Final Art

Use placeholder assets.

The goal is to test gameplay.

---

# Suggested First Vertical Slice

The smallest meaningful version of the game is:

```text
One Arena
    ↓
One Cart
    ↓
One Rider
    ↓
One Shooter
    ↓
One Weapon
    ↓
One Enemy
    ↓
Enemy Drops Beer
    ↓
Shooter Drinks Beer
    ↓
Shooter Becomes Stronger
    ↓
Cart Becomes Harder to Control
    ↓
Rider Adapts
    ↓
Level Up
    ↓
Choose Upgrade
    ↓
Survive
```

This is enough to determine whether the game's central idea works.

---

# Core Development Milestones

## Milestone 1 — Fun Cart

Can the Rider enjoy controlling the cart without combat?

---

## Milestone 2 — Fun Combat

Can the Shooter enjoy attacking enemies?

---

## Milestone 3 — Fun Cooperation

Does the Rider's movement meaningfully affect the Shooter?

---

## Milestone 4 — Fun Beer

Does the Shooter genuinely want to drink beer despite the consequences?

---

## Milestone 5 — Fun Progression

Do upgrades create interesting decisions?

---

## Milestone 6 — Fun Ten-Minute Run

Would players voluntarily start another run?

---

# The Most Important Playtest Questions

After each prototype session, ask the players:

### Rider

* Did driving feel fun?
* Did you feel like you had meaningful control?
* Did you make interesting movement decisions?
* Did intoxication create an interesting challenge?
* Did the cart feel like a weapon?

### Shooter

* Was shooting satisfying?
* Did you care about positioning?
* Did you want to drink beer?
* Did you feel that your choices affected the Rider?

### Both

* Did you communicate naturally?
* Did you disagree about what to do?
* Did you feel like you were playing the same game?
* Did one role feel less important?
* Did you want to play another run?

---

# Success Criteria

The prototype is successful if:

```text
The Rider enjoys driving
        AND
The Shooter enjoys fighting
        AND
The players need each other
        AND
Beer creates meaningful risk
        AND
The game becomes more interesting as it becomes more chaotic
```

The game does not need to be polished.

It does not need extensive content.

It does not need a complete roguelike progression system.

It only needs to prove:

> **The shared shopping cart creates gameplay that is more fun than simply playing a normal single-player survivor-like game.**

---

# Final Prototype Principle

Build the game in the order of uncertainty.

The biggest unknown is not:

> **Can a roguelike progression system be implemented?**

That is straightforward.

The biggest unknown is:

> **Can controlling a shopping cart be fun enough to support an entire player role?**

Therefore, the first serious prototype should focus on:

```text
Cart
    +
Momentum
    +
Combat
    +
Cooperation
    +
Beer
```

Everything else comes later.

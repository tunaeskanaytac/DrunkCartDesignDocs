# Technical Prototype Plan

## Purpose

The purpose of this prototype is to answer one question:

> **Is driving a shopping cart while another player fights enemies actually fun?**

The prototype should not attempt to build the full game.

It should not contain:

* A complete progression system
* Multiple worlds
* Dozens of enemies
* A large weapon system
* Procedural generation
* Final art
* A complete UI
* A full run structure

The prototype exists to validate the core gameplay.

---

# The Prototype's Core Question

The game should eventually be:

```text
Rider
    +
Shooter
    +
Shopping Cart
    +
Enemies
    +
Beer
    ↓
Chaotic Cooperative Combat
```

The prototype should test whether this is fun without relying on:

* Story
* Visual polish
* Content quantity
* Progression
* Unlocks

If the basic interaction is not fun, more content will not fix it.

---

# Prototype Scope

The prototype should contain:

## Two Players

* One Rider
* One Shooter

---

## One Cart

The cart should support:

* Acceleration
* Braking
* Steering
* Momentum
* Collision

---

## One Weapon

The Shooter should have:

* Aim
* Fire
* Basic damage

---

## Three Enemy Types

Enough to test different combat situations.

---

## One Beer System

The prototype should include:

* Beer pickups
* Drinking
* Intoxication
* Shooter benefits
* Rider penalties

---

## One Small Level

The level should contain:

* Open space
* Narrow space
* Obstacles
* A ramp or special movement feature
* Beer rewards

---

## One Run

The prototype does not need a full roguelike structure yet.

It only needs:

```text
Start
    ↓
Fight
    ↓
Collect Beer
    ↓
Become Stronger
    ↓
Become More Difficult to Control
    ↓
Fight More Enemies
    ↓
Win or Die
```

---

# Prototype Development Order

The prototype should be built in the following order:

```text
1. Cart Movement
        ↓
2. Shooter Interaction
        ↓
3. Basic Enemy
        ↓
4. Combat Loop
        ↓
5. Beer System
        ↓
6. Intoxication
        ↓
7. Level Interaction
        ↓
8. Multiplayer Stress Test
```

The order is important.

Do not build progression before knowing whether the basic vehicle is fun.

---

# Phase 0: Technical Foundation

## Goal

Create the smallest possible playable scene.

The scene should contain:

```text
Scene
├── Cart
│   ├── Rider Controller
│   └── Shooter Controller
├── Camera
├── Ground
└── Test Objects
```

The scene should have no unnecessary systems.

---

# Input

The prototype should use the Unity Input System.

The two players should be able to control their roles independently.

## Rider Inputs

* Accelerate
* Brake / Reverse
* Steer Left
* Steer Right
* Ram / Boost
* Interact

---

## Shooter Inputs

* Aim
* Fire
* Ability
* Drink Beer

The input system should allow the controls to be replaced later.

The prototype should not hardcode input logic into gameplay systems.

---

# Phase 1: Cart Movement

## Goal

Determine whether the cart is fun to control.

This is the most important phase.

The cart should initially support:

```text
Accelerate
    ↓
Build Momentum
    ↓
Steer
    ↓
Brake
    ↓
Collide
```

---

# Movement Model

The initial controller should be arcade-oriented.

Do not begin with a realistic shopping cart simulation.

The desired feeling is:

> **Easy to understand, difficult to master.**

The player should quickly understand:

* How to accelerate
* How to turn
* How to stop

But skilled players should improve at:

* Maintaining momentum
* Drifting
* Braking
* Ramming

---

# Movement Variables

The movement controller should expose parameters such as:

```text
Max Speed
Acceleration
Braking Force
Turn Speed
Steering Response
Traction
Momentum Retention
Reverse Speed
```

These should be adjustable in the Inspector.

The purpose is rapid iteration.

---

# Movement Test Arena

Create a test arena containing:

```text
┌──────────────────────────────┐
│                              │
│       Open Area              │
│                              │
│   ┌──────┐        ┌──────┐   │
│   │      │        │      │   │
│   │ Wall │        │ Wall │   │
│   │      │        │      │   │
│   └──────┘        └──────┘   │
│                              │
│          Ramp                │
│            ▲                 │
│                              │
└──────────────────────────────┘
```

The Rider should be able to test:

* Straight-line speed
* Turning
* Braking
* Collision
* Ramps

---

# Movement Success Test

The Rider should be able to answer:

> **I want to drive around for five minutes even when nothing is happening.**

If the answer is no:

> **Stop development and improve the driving.**

This is the most important prototype gate.

---

# Phase 2: Shooter Integration

## Goal

Make the cart a combat platform.

The Shooter should be able to:

```text
Aim
    ↓
Shoot
    ↓
Hit Targets
    ↓
Deal Damage
```

The Rider should be able to:

```text
Drive
    ↓
Position Cart
    ↓
Create Shooting Opportunities
```

---

# First Weapon

The first weapon should be extremely simple.

For example:

```text
Automatic Weapon
    ↓
Constant Fire Rate
    ↓
Projectile
    ↓
Damage
```

Do not begin with:

* Multiple weapons
* Complex reloads
* Skill trees
* Elemental systems

The goal is to test:

> **Does the Rider's movement make the Shooter's combat more interesting?**

---

# Shooter Targeting

The Shooter should be able to aim independently of the Rider.

This is essential.

The Rider controls:

> **Movement direction.**

The Shooter controls:

> **Combat direction.**

This is the fundamental two-player interaction.

---

# Shooter Test

Create several stationary targets.

The Rider should drive around them while the Shooter aims.

Then ask:

* Is aiming while moving fun?
* Does the Rider's movement create interesting angles?
* Does the Shooter feel dependent on positioning?
* Is the Shooter frustrated by vehicle movement?

---

# Phase 3: First Enemy

## Goal

Create the first combat loop.

The first enemy should be simple.

```text
Enemy
    ↓
Approaches Cart
    ↓
Shooter Fires
    ↓
Enemy Dies
    ↓
Reward Drops
```

The enemy should not require complex AI.

The purpose is to test:

> **Does movement plus combat create an enjoyable loop?**

---

# Recommended First Enemy

A basic melee enemy.

It should:

* Move toward the cart
* Damage the cart on contact
* Die when shot

This is enough.

---

# Enemy Interaction With the Rider

The Rider should be able to interact with the enemy through movement.

For example:

```text
Cart
    ↓
High-Speed Collision
    ↓
Enemy Takes Damage
```

This is important.

The Rider must have an offensive action.

Otherwise:

> **The Shooter is the only player actually killing enemies.**

---

# Phase 4: First Enemy Group

Once one enemy works, add multiple enemies.

The first combat scenario should look like:

```text
        Enemy
          ↓

Enemy → CART ← Enemy

          ↑
        Enemy
```

The team must:

* Move
* Aim
* Shoot
* Avoid
* Ram

This is the first real test of cooperation.

---

# Phase 5: Enemy Variety

Only after the basic enemy works should additional enemies be added.

The prototype needs three enemy roles.

---

## Enemy 1: Basic Melee

Purpose:

> **Creates constant pressure.**

---

## Enemy 2: Ranged Enemy

Purpose:

> **Punishes staying in one location.**

The Rider must keep moving.

---

## Enemy 3: Control Enemy

Examples:

* Grabber
* Slow enemy
* Stunner
* Wall creator

Purpose:

> **Creates a problem that must be prioritized.**

The Shooter must make target decisions.

---

# Enemy Prototype Rule

Every enemy should answer:

> **What does this enemy make the Rider do?**

and:

> **What does this enemy make the Shooter do?**

If the answer is:

> **Nothing different.**

The enemy probably does not belong in the prototype.

---

# Phase 6: Beer System

## Goal

Test the central risk/reward mechanic.

The first version should be extremely simple.

```text
Enemy Dies
    ↓
Beer Drops
    ↓
Rider Collects Beer
    ↓
Shared Beer Count Increases
    ↓
Team Drinks
    ↓
Intoxication Increases
```

---

# Beer Prototype

The team should have:

```text
Beer: 0
Intoxication: 0%
```

Collecting beer:

```text
Beer += 1
```

Drinking beer:

```text
Beer -= 1
Intoxication += 10%
```

The numbers are placeholders.

The important thing is the relationship.

---

# Intoxication Effects

Start with only two effects.

## Shooter

```text
Intoxication
    ↓
Increased Damage
```

## Cart

```text
Intoxication
    ↓
Increased Momentum
```

This is enough to test the core tradeoff.

---

# Beer Prototype Question

The team should naturally ask:

> **Should we drink this?**

If drinking beer is always correct:

> **The system has no meaningful decision.**

If drinking beer is always bad:

> **The reward is not attractive enough.**

The ideal situation is:

> **We want the power, but we are afraid of the consequences.**

---

# Phase 7: Intoxication Thresholds

Once the basic beer system works, add stages.

Example:

```text
0%
Normal

25%
Shooter Damage Increase

50%
More Cart Momentum

75%
Reduced Shooter Accuracy

100%
Extreme Handling
```

These effects should be tested one at a time.

Do not add every effect simultaneously.

---

# Phase 8: Level Interaction

The prototype level should now contain:

```text
Open Area
    ↓
Narrow Route
    ↓
Obstacle Section
    ↓
Ramp
    ↓
Reward Area
```

The team should need to navigate the environment while fighting.

---

# Level Test

The Rider should make decisions such as:

> **Do I take the narrow shortcut?**

> **Do I go around the obstacle?**

> **Do I risk getting the beer?**

> **Can I make this turn while drunk?**

These decisions are the foundation of the final game.

---

# Phase 9: Cart as a Weapon

The Rider should receive a basic offensive ability.

Start with:

> **Ram.**

The simplest version:

```text
High Speed
    ↓
Collision
    ↓
Enemy Takes Damage
```

Possible additions later:

* Knockback
* Damage scaling with speed
* Stun
* Destruction
* Combo bonuses

The first test should simply answer:

> **Does ramming enemies feel good?**

---

# Phase 10: Cooperative Abilities

Only after both players have satisfying individual gameplay should cooperative abilities be added.

A simple example:

```text
Shooter Marks Enemy
        ↓
Rider Ramming Enemy
        ↓
Bonus Damage
```

This creates:

```text
Shooter
    ↓
Creates Target
    +
Rider
    ↓
Executes Attack
```

The players should feel like they are combining their abilities.

---

# Phase 11: Basic Run

The prototype can now have a minimal run.

```text
Start
    ↓
Enemy Group
    ↓
Reward
    ↓
Enemy Group
    ↓
Elite Enemy
    ↓
Reward
    ↓
Final Encounter
```

The run should last approximately:

> **10–20 minutes.**

It does not need to be procedurally generated.

---

# Minimal Progression

The prototype should include only a few upgrades.

For example:

## Rider Upgrade

> +10% acceleration

---

## Shooter Upgrade

> +10% damage

---

## Beer Upgrade

> Intoxication has a stronger effect

---

## Shared Upgrade

> Increased cart health

This is enough to test whether upgrades create interesting choices.

---

# Prototype Run Structure

A simple run can be:

```text
┌─────────────┐
│ Start       │
└──────┬──────┘
       ↓
┌─────────────┐
│ Enemy Wave  │
└──────┬──────┘
       ↓
┌─────────────┐
│ Beer Reward │
└──────┬──────┘
       ↓
┌─────────────┐
│ Enemy Wave  │
└──────┬──────┘
       ↓
┌─────────────┐
│ Upgrade     │
└──────┬──────┘
       ↓
┌─────────────┐
│ Elite       │
└──────┬──────┘
       ↓
┌─────────────┐
│ Final Fight │
└─────────────┘
```

This is enough.

---

# Technical Architecture

The prototype should be modular enough to allow fast iteration.

A possible structure:

```text
Game
├── GameManager
├── RunManager
├── Combat
├── Progression
├── Beer
├── Cart
│   ├── CartMovement
│   ├── CartHealth
│   └── CartCombat
├── Rider
├── Shooter
├── Enemies
└── UI
```

The architecture should not be over-engineered.

The purpose is to make changing values easy.

---

# Recommended Component Separation

## CartMovement

Responsible for:

* Velocity
* Acceleration
* Steering
* Braking

---

## CartCombat

Responsible for:

* Ram damage
* Collision attacks
* Boosts

---

## CartHealth

Responsible for:

* Damage
* Healing
* Death

---

## BeerSystem

Responsible for:

* Beer inventory
* Drinking
* Intoxication

---

## IntoxicationModifier

Responsible for applying intoxication effects.

For example:

```text
Intoxication
    ↓
Modifier
    ↓
Movement Parameters
```

This keeps the movement system from needing to understand beer directly.

---

# Avoid This

Do not write:

```text
if (beer > 5)
{
    movementSpeed *= 0.5f;
}
```

inside the cart movement controller.

Instead:

```text
Intoxication System
        ↓
Movement Modifier
        ↓
Cart Movement
```

The systems should communicate through data or modifiers.

This will make future upgrades much easier.

---

# Data-Driven Design

Important values should be editable without rewriting code.

Examples:

```text
CartStats
├── Max Speed
├── Acceleration
├── Turn Speed
├── Braking
└── Traction
```

```text
WeaponStats
├── Damage
├── Fire Rate
├── Range
└── Projectile Speed
```

```text
IntoxicationEffects
├── Damage Modifier
├── Momentum Modifier
├── Accuracy Modifier
└── Handling Modifier
```

For Unity, ScriptableObjects are a good fit for these definitions.

---

# Prototype Debug Tools

The prototype should include debug tools from the beginning.

Useful debug controls:

```text
F1
Add Beer

F2
Increase Intoxication

F3
Spawn Enemy

F4
Kill All Enemies

F5
Reset Cart

F6
Increase Speed
```

These tools dramatically accelerate iteration.

Do not make yourself play through the entire game to test one mechanic.

---

# Debug UI

Display:

```text
Speed: 12.4
Intoxication: 60%
Beer: 3
Cart Health: 72%
Enemy Count: 14
```

This makes tuning easier.

The final game does not need to display all of this.

---

# Multiplayer Testing

The multiplayer prototype should be tested early.

Do not wait until the entire game is finished.

The basic question is:

> **Does the game remain fun when controlled by two real people?**

---

# Multiplayer Test Order

## First

Both players on the same computer.

This is useful for debugging.

---

## Second

Two local players with separate controllers.

This tests:

* Input
* Camera
* Role separation

---

## Third

Networked multiplayer.

Only after the gameplay is proven locally.

---

# Network Architecture

Do not make networking the first problem.

The recommended development order is:

```text
Single-Player Simulation
        ↓
Two Local Players
        ↓
Networked Multiplayer
```

The game should be fun before networking complexity is added.

---

# Simulating the Other Player

During early development, one player can control both roles.

For example:

```text
Keyboard
    ↓
Rider

Controller
    ↓
Shooter
```

This allows rapid testing.

However:

> **Do not trust single-player testing alone.**

The final game must eventually be tested with two real players.

---

# Prototype Milestones

## Milestone 1: Driving

The Rider can:

* Accelerate
* Steer
* Brake
* Collide

### Question

> **Is the cart fun to drive?**

---

## Milestone 2: Combat

The Shooter can:

* Aim
* Shoot
* Kill enemies

### Question

> **Does movement make shooting more interesting?**

---

## Milestone 3: Cooperation

Both roles interact.

### Question

> **Do the players need each other?**

---

## Milestone 4: Beer

Beer creates:

* Power
* Risk
* Handling changes

### Question

> **Is drinking a meaningful decision?**

---

## Milestone 5: Environment

The level creates:

* Routes
* Obstacles
* Ramps
* Rewards

### Question

> **Does the Rider interact with the world?**

---

## Milestone 6: Run

The game has:

* Multiple encounters
* Rewards
* Upgrades
* A final encounter

### Question

> **Would we play another run?**

---

# The Vertical Slice

The first real target should be a tiny vertical slice.

It should contain:

```text
1 Cart
2 Players
3 Enemy Types
1 Weapon
1 Rider Ability
1 Small Level
1 Beer System
5–10 Upgrades
1 Elite Encounter
1 Final Encounter
```

The entire slice should be playable from beginning to end.

---

# The Vertical Slice Experience

The player should experience:

```text
Start
    ↓
Learn Driving
    ↓
Fight Enemies
    ↓
Collect Beer
    ↓
Become Stronger
    ↓
Become More Difficult to Control
    ↓
Make Upgrade Choices
    ↓
Fight Stronger Enemies
    ↓
Reach Final Encounter
    ↓
Win or Die
```

If this small experience is fun:

> **The game has a foundation.**

---

# What Not to Build Yet

Do not build these before validating the core loop:

## Large Content Systems

* 20 enemy types
* 50 weapons
* 10 worlds

---

## Complex Meta-Progression

* Permanent unlock trees
* Currency systems
* Character progression

---

## Online Infrastructure

* Matchmaking
* Dedicated servers
* Lobby systems

---

## Final Presentation

* Cinematics
* Voice acting
* Final UI
* Extensive VFX

---

## Procedural Generation

Do not procedurally generate a game that has not yet proven its core movement.

---

# The Prototype Kill Criteria

The prototype should be allowed to fail.

Possible outcomes:

## Result 1

> **Driving is fun.**

Continue developing the game.

---

## Result 2

> **Driving is fun, but the Shooter is not engaged enough.**

Improve Shooter interaction.

---

## Result 3

> **Shooting is fun, but driving is not.**

Rework the cart controller or level design.

---

## Result 4

> **The two roles do not need each other.**

Rework the cooperative design.

---

## Result 5

> **Beer is not interesting.**

Replace or redesign the beer system.

---

## Result 6

> **The entire combination is fun.**

You have found the game's core.

---

# The Most Important Playtest

Do not ask:

> **Is this game good?**

Ask specific questions.

### Rider

> **Would you keep driving if there were no enemies?**

### Shooter

> **Does the Rider's movement create interesting combat?**

### Team

> **Did you communicate because the game required it?**

### Beer

> **Did you ever want to drink beer despite the risk?**

### Failure

> **Did you laugh when something went wrong?**

### Replay

> **Would you immediately play another run?**

These questions provide much better information.

---

# Recommended Development Sequence

The actual development plan should be:

```text
Week 1
Cart Movement

Week 2
Shooter Integration

Week 3
Basic Combat

Week 4
Multiplayer Interaction

Week 5
Beer and Intoxication

Week 6
Environment Interaction

Week 7
Basic Run Structure

Week 8
Playtesting and Rework
```

These are not strict deadlines.

The important principle is:

> **Do not move to the next phase until the current phase is fun enough to justify continuing.**

---

# The Prototype's Definition of Done

The prototype is successful when:

```text
Two players
    ↓
Control one cart
    ↓
Fight enemies
    ↓
Move through a level
    ↓
Collect beer
    ↓
Become stronger
    ↓
Become harder to control
    ↓
Make upgrade choices
    ↓
Reach a final encounter
    ↓
Want to play again
```

The game does not need to be polished.

It does not need to be beautiful.

It does not need a large amount of content.

It needs to prove one thing:

> **Two friends controlling one increasingly drunk shopping cart is a fun game.**

---

# Final Development Principle

The project should be developed from the inside out.

```text
Fun Driving
        ↓
Fun Combat
        ↓
Fun Cooperation
        ↓
Fun Beer Decisions
        ↓
Fun Level Interaction
        ↓
Fun Run Structure
        ↓
Progression
        ↓
Content
        ↓
Polish
```

Do not reverse this order.

Do not spend months designing:

* Enemy lore
* Procedural worlds
* Upgrade trees
* Meta-progression

before answering:

> **Is the cart itself fun?**

The shopping cart is the game's biggest risk.

It is also its biggest opportunity.

If driving the cart is genuinely fun, the game has a unique foundation that separates it from the hundreds of other roguelikes.

If driving is not fun, the project needs to discover that as early as possible.

The prototype exists to find out.

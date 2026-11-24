# Shopping Cart Roguelike — Game Ideas

## High Concept

A cooperative friendslop roguelike where:

* One player rides and controls a shopping cart.
* Another player sits in the cart and fights enemies.
* Enemies drop beer.
	> Initial idea. I'd prefer if enemies dropped some kind of currency which you can spend to obtain beers.
* Drinking beer makes the shooter more powerful.
* However, intoxication makes the cart and its controls increasingly difficult to handle.

> **One player drives the shopping cart while the other gets drunk, shoots monsters, and makes everything progressively more chaotic.**

The game's primary identity should come from the interaction between the two players, rather than simply being another single-player survivor-like game.

---

# Core Design Question

The game could technically be a single-player roguelike. However, there are already many single-player survivor-like and roguelike games.

The multiplayer version has a stronger unique premise:

> **One player controls the vehicle while the other controls the weapon.**

The key question is:

> **What can the second player do that creates gameplay a single-player version cannot reproduce?**

The answer should be a meaningful difference in gameplay rather than simply adding a second player to a normal roguelike.

---

# Core Gameplay Loop

```text
Explore
    ↓
Fight enemies
    ↓
Collect beer / rewards
    ↓
Drink beer
    ↓
Become more powerful
    ↓
Become more difficult to control
    ↓
Survive
    ↓
Level up
    ↓
Choose upgrades
    ↓
Repeat
```

The most important risk/reward relationship is:

> **Beer makes the shooter stronger but makes the vehicle harder to control.**

This naturally creates cooperation and conflict between the two players.

---

# Player Roles

## The Shooter

The shooter controls the offensive side of the game.

Possible responsibilities:

* Aim
* Shoot enemies
* Choose targets
* Collect beer
* Drink beer
* Choose shooter upgrades
* Manage their intoxication

The shooter wants:

* More enemies
* More kills
* More beer
* More power
* More risky opportunities

---

## The Rider

The rider controls the vehicle and should not simply be a glorified steering wheel.

The rider should have their own gameplay loop and progression.

Possible responsibilities:

* Steering
* Managing momentum
* Braking
* Drifting
* Positioning the shooter
* Avoiding obstacles
* Running over enemies
* Using vehicle abilities
* Choosing rider/cart upgrades

The rider wants:

* Good positioning
* Control
* Space
* Safe escape routes
* Manageable levels of intoxication

This naturally creates tension between the players.

Example:

> **Shooter:** “There's a huge group of enemies over there!”
>
> **Rider:** “We're going the other way.”
>
> **Shooter:** “But there's beer!”
>
> **Rider:** “I don't care!”
>
> **Shooter:** “I'm drinking it.”
>
> **Rider:** “NO—”

This type of interaction is one of the game's biggest potential strengths.

---

# The Rider Should Be a Vehicle Combat Role

The rider should not only move the cart from point A to point B.

The cart itself should be a gameplay tool and potentially a weapon.

The rider should constantly make decisions such as:

```text
Enemy group approaching
        ↓
Do I:
  ├─ Turn sharply and escape?
  ├─ Maintain momentum and ram through?
  ├─ Brake so the shooter can aim?
  ├─ Drift around the group?
  └─ Boost toward the beer?
```

The goal is for the rider to make interesting decisions every few seconds.

A useful design test:

> **Can the rider make interesting decisions every five seconds?**

If the rider only holds forward and occasionally turns, the role is probably not deep enough.

---

# Potential Rider Mechanics

## Momentum

The cart should have meaningful momentum.

The rider must think ahead:

> **Where do I want to be in three seconds?**

Potential characteristics:

* Difficult to stop instantly
* Speed affects turning
* Momentum must be managed
* Braking has a cost
* High speed enables risky maneuvers

The driving loop could be:

```text
Position
    ↓
Build momentum
    ↓
Make a risky maneuver
    ↓
Escape or attack
    ↓
Reposition
```

---

## Drift

The rider can rotate the cart while maintaining momentum.

Uses:

* Dodging enemies
* Repositioning the shooter
* Making sharp turns
* Maintaining speed through corners

---

## Handbrake Turn

Allows a sharp turn at the cost of speed.

Potentially useful for:

* Emergency escapes
* Avoiding obstacles
* Turning toward enemies
* Repositioning the shooter

---

## Boost

A short burst of speed.

Possible uses:

* Escape
* Chase beer
* Ram enemies
* Cross dangerous areas
* Perform risky maneuvers

---

## Ram

The cart can intentionally become a weapon.

Possible upgrades could increase:

* Collision damage
* Knockback
* Speed-based damage
* Area of impact
* Enemy penetration

This allows the rider to have an offensive playstyle independent of the shooter.

---

## Other Possible Vehicle Abilities

Potential future mechanics:

* Jump
* Ground slam
* Shield
* Temporary invulnerability
* Grappling hook
* Turning boost
* Shockwave on collision
* Ability to push enemies into other enemies

These should be added only if the basic driving loop needs more depth.

---

# Beer System

Beer is potentially the game's central mechanic.

It should not simply be a health potion or generic experience item.

The core relationship is:

```text
More Beer
    ↓
More Power
    ↓
More Intoxication
    ↓
More Difficult Control
```

The shooter may want to become increasingly drunk because the benefits are worth the risk.

The rider may want the shooter to stop drinking because the cart is becoming harder to control.

---

# Possible Intoxication Levels

```text
Sober
  ↓
Tipsy
  ↓
Drunk
  ↓
Wasted
```

## Sober

* Normal abilities
* Normal controls

## Tipsy

* Slightly increased power
* Mild camera sway
* Minor control changes

## Drunk

* Increased damage
* Increased attack speed
* More camera sway
* More difficult aiming
* More difficult vehicle handling

## Wasted

* Extremely powerful abilities
* Strong control challenges
* Major screen effects
* Exaggerated momentum
* High risk of losing control

The important distinction:

> Intoxication should create difficulty the player can learn to manage, rather than pure randomness.

For example:

### Better

> The cart has exaggerated momentum while drunk.

### Worse

> The cart randomly turns left.

The first creates a skill challenge. The second simply removes player agency.

---

# Player Conflict as a Game Mechanic

The shooter and rider should have different priorities.

## Shooter

Wants:

* More enemies
* More kills
* More beer
* More power
* More risk

## Rider

Wants:

* Safe positioning
* Space
* Control
* Clear escape routes
* Manageable intoxication

This creates a cooperative conflict:

```text
Shooter:
"I want to go toward the enemies."

Rider:
"I want to avoid the enemies."

Shooter:
"I want to drink this beer."

Rider:
"You're already too drunk."

Shooter:
"I need the damage."

Rider:
"We are going to crash."
```

This conflict is potentially something that a single-player game cannot naturally recreate.

---

# Roguelike Progression

The game should have separate progression paths for the shooter and the rider.

## Shooter Upgrades

Possible upgrades:

* Damage
* Fire rate
* Projectile count
* Projectile size
* Pierce
* Explosions
* Homing projectiles
* Critical hits
* Chain lightning
* Lifesteal
* Beer generation
* Intoxication bonuses

Example:

### Double Shot

> Fire an additional projectile.

### Cheap Booze

> Beer provides more power but increases intoxication faster.

### Bottomless Mug

> Drinking beer temporarily increases fire rate.

---

## Rider / Cart Upgrades

Possible upgrades:

* Acceleration
* Maximum speed
* Turning
* Braking
* Drift control
* Collision damage
* Armor
* Boost charges
* Traction
* Momentum control

Example:

### Shopping Cart Wheel Alignment

> Turning becomes more responsive.

### Reinforced Basket

> Collisions deal less damage.

### Unnecessary Speed

> Maximum speed increases, but braking becomes worse.

---

# Possible Build Archetypes

## Machine Gun Alcoholic

Characteristics:

* Extremely high fire rate
* Many projectiles
* High intoxication
* Poor accuracy

The rider has to deal with a powerful but increasingly chaotic shooter.

---

## Demolition Cart

Characteristics:

* High rider speed
* Powerful collisions
* Explosive impacts
* Shooter provides supporting fire

The cart itself becomes the primary weapon.

---

## Sniper

Characteristics:

* High damage
* Slow fire rate
* Precise aiming
* Low intoxication

The shooter attempts to remain sober and accurate while the rider positions them.

---

## Chaos Build

Characteristics:

* Random projectiles
* Explosions
* Chain reactions
* Maximum intoxication

The build intentionally embraces unpredictability.

---

# The Game's Possible Identity

The game should not simply be:

> **A cooperative Vampire Survivors clone with a shopping cart.**

A stronger identity would be:

> **A cooperative survivor-like game where one player controls the vehicle and the other controls the weapon—and the weapon player can become increasingly powerful by making the vehicle harder to control.**

Or more simply:

> **Two players share one increasingly powerful and increasingly uncontrollable shopping cart.**

---

# Prototype Goals

Do not build the full game immediately.

The first important test is a small vertical slice.

## Prototype Contents

* One arena
* One shopping cart
* One rider
* One shooter
* One basic weapon
* Three enemy types
* Beer drops
* Intoxication system
* Basic rider upgrades
* Basic shooter upgrades
* Level-up choices
* A 10-minute survival objective

---

# Suggested Enemy Types

## Chaser

* Runs directly toward the cart
* Tests movement and positioning

## Ranged Enemy

* Attacks from a distance
* Forces the rider to reposition

## Large Enemy

* Slow but dangerous
* Creates decisions about whether to fight or avoid it

---

# First Prototype Test

The first serious prototype should answer:

> **Is riding around together while one player gets progressively drunk and stronger fun for ten minutes?**

The game does not need:

* Permanent meta-progression
* Many maps
* Large amounts of content
* Complex menus
* Extensive lore
* Many weapons

At this stage, the goal is to validate the core interaction.

---

# Rider Gameplay Test

The rider should be able to answer "yes" to most of these questions:

1. Can I outmaneuver enemies?
2. Can I use momentum skillfully?
3. Can I make risky plays?
4. Can I choose where to position the shooter?
5. Can I use the cart as a weapon?
6. Can I improve the cart through upgrades?

If the rider is only steering and occasionally turning, the multiplayer role probably needs more depth.

---

# Core Design Question

The most important question for the project is:

> **Can two players with different goals make each other more powerful and more incompetent at the same time?**

If the answer is yes, the game has a strong multiplayer identity.

The central fantasy is:

> **The shooter wants to become stronger. The rider wants to remain in control. Beer gives the shooter what they want while making the rider's job increasingly difficult.**

That tension is the foundation of the game.

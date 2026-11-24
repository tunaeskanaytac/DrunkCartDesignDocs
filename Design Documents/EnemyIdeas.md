# Enemy Design

## Purpose

Enemies should create meaningful decisions for both players.

The enemies should not simply:

> **Walk toward the cart and absorb bullets.**

Each enemy should create a specific problem involving:

* Position
* Movement
* Target priority
* Momentum
* Escape routes
* Intoxication
* Communication

The core design principle is:

> **Every important enemy should create a problem that the Rider and Shooter solve differently.**

---

# Enemy Design Philosophy

The game has two player roles:

## Rider

Controls:

* Position
* Momentum
* Escape
* Collision
* Team movement

## Shooter

Controls:

* Damage
* Target selection
* Threat removal
* Reward generation

Therefore, enemies should create situations where:

```text
Enemy Creates Problem
        ↓
Rider Chooses Position
        +
Shooter Chooses Target
        ↓
Team Solves Problem
```

---

# The Enemy Design Question

For every enemy, ask:

> **What does this enemy force the Rider to do?**

And:

> **What does this enemy force the Shooter to do?**

If the answer is:

> **Nothing different from any other enemy**

then the enemy probably does not need to exist.

---

# Enemy Roles

Enemies should generally belong to functional categories.

```text
Chasers
    ↓
Area Denial
    ↓
Ranged Threats
    ↓
Disruptors
    ↓
Tanks
    ↓
Elites
    ↓
Bosses
```

Different enemy types should create different spatial problems.

---

# Enemy 1 — The Chaser

## Role

The basic enemy.

The Chaser moves toward the cart and attacks at close range.

```text id="j2k5b9"
Find Cart
    ↓
Move Toward Cart
    ↓
Attack
```

## What It Tests

The Chaser tests:

* Basic movement
* Target priority
* Ramming
* Escape routes

## Rider Response

The Rider can:

* Avoid it
* Ram it
* Maintain distance
* Lead it into other enemies

## Shooter Response

The Shooter can:

* Kill it
* Ignore it
* Use it to generate rewards

The Chaser should be the basic enemy against which all other enemies are compared.

---

# Enemy 2 — The Swarm

## Role

Creates large numbers of weak enemies.

The Swarm is individually weak but dangerous in groups.

## Purpose

The Swarm tests:

* Area damage
* Movement
* Crowd control
* Positioning

## Rider Response

The Rider must:

* Avoid being surrounded
* Maintain momentum
* Create space

## Shooter Response

The Shooter must:

* Prioritize area damage
* Kill enemies blocking escape routes
* Prevent the swarm from reaching the cart

The Swarm should create:

> **The problem of space.**

---

# Enemy 3 — The Ranged Enemy

## Role

Attacks the cart from a distance.

Possible attacks:

* Projectiles
* Spikes
* Energy attacks
* Thrown objects

The Ranged Enemy should avoid directly approaching the cart.

```text id="51x6i2"
Maintain Distance
    ↓
Attack Cart
    ↓
Reposition
```

## Rider Response

The Rider must:

* Move unpredictably
* Close distance
* Find cover
* Prioritize the enemy's location

## Shooter Response

The Shooter must:

* Identify the threat
* Aim at a distant target
* Decide whether it is worth pursuing

The Ranged Enemy creates:

> **The problem of distance.**

---

# Enemy 4 — The Blocker

## Role

Creates physical obstacles.

The Blocker may:

* Have high health
* Stand in narrow paths
* Create a wall
* Protect other enemies

The Rider cannot simply ignore it.

## Rider Response

The Rider can:

* Go around
* Ram it
* Slow down
* Find another route

## Shooter Response

The Shooter can:

* Kill it
* Attack enemies behind it
* Target a weak point

The Blocker creates:

> **The problem of pathing.**

---

# Enemy 5 — The Grabber

## Role

Disrupts movement.

Possible behavior:

* Pulls the cart
* Slows the cart
* Hooks onto the cart
* Attempts to drag the vehicle

This enemy should threaten the Rider's control.

## Rider Response

The Rider must:

* Avoid being grabbed
* Break free
* Use movement abilities

## Shooter Response

The Shooter must:

* Quickly kill the Grabber
* Prioritize it over less dangerous targets

The Grabber creates:

> **The problem of control.**

---

# Enemy 6 — The Spitter

## Role

Creates temporary environmental hazards.

The Spitter may leave:

* Acid
* Slime
* Fire
* Sticky terrain
* Poison clouds

The hazard should remain in the arena temporarily.

## Rider Response

The Rider must:

* Avoid dangerous terrain
* Plan escape routes
* Adjust movement

## Shooter Response

The Shooter must:

* Kill the Spitter before the arena becomes difficult to navigate

The Spitter creates:

> **The problem of changing terrain.**

---

# Enemy 7 — The Kamikaze Enemy

## Role

Attempts to collide with the cart.

The enemy may:

* Explode
* Deal massive impact damage
* Create knockback

The Rider should have the option to avoid it.

## Rider Response

The Rider can:

* Dodge
* Ram it first
* Use a boost
* Lead it away

## Shooter Response

The Shooter can:

* Kill it at range
* Prioritize it before it reaches the cart

The Kamikaze enemy creates:

> **The problem of timing.**

---

# Enemy 8 — The Leech

## Role

Steals resources.

Possible behaviors:

* Steals beer
* Steals experience
* Steals temporary powerups
* Runs away with rewards

The team must choose whether to pursue it.

## Rider Response

The Rider may need to:

* Chase it
* Take a dangerous route
* Abandon other threats

## Shooter Response

The Shooter must:

* Kill it quickly
* Decide whether the reward is worth the risk

The Leech creates:

> **The problem of greed.**

---

# Enemy 9 — The Drunkard

## Role

Interacts directly with intoxication.

Possible behaviors:

* Increases the team's intoxication
* Throws beer
* Drops large amounts of beer
* Becomes stronger when the team is drunk

This enemy should connect directly to the game's central mechanic.

## Rider Response

The Rider must decide:

> **Do we want to fight this enemy?**

## Shooter Response

The Shooter must decide:

> **Do we want the reward?**

The Drunkard creates:

> **The problem of temptation.**

---

# Enemy 10 — The Disruptor

## Role

Temporarily changes the vehicle's handling.

Possible effects:

* Increased momentum
* Reduced traction
* Reduced acceleration
* Inverted steering
* Reduced braking

The effect should be temporary and predictable.

## Rider Response

The Rider must adapt.

## Shooter Response

The Shooter must prioritize the Disruptor if the handling change is dangerous.

The Disruptor creates:

> **The problem of adaptation.**

---

# Enemy 11 — The Shielded Enemy

## Role

Creates a target-selection problem.

The Shielded Enemy may:

* Reduce damage from the front
* Protect nearby enemies
* Require attacking from a specific direction

## Rider Response

The Rider must reposition the cart.

## Shooter Response

The Shooter must find the correct angle.

The Shielded Enemy creates:

> **The problem of positioning.**

---

# Enemy 12 — The Support Enemy

## Role

Makes other enemies stronger.

Possible effects:

* Healing
* Damage buffs
* Speed buffs
* Shielding
* Enemy resurrection

The Support Enemy should not necessarily be the strongest enemy.

It should be a priority target.

## Rider Response

The Rider may need to position the Shooter toward it.

## Shooter Response

The Shooter must decide whether to abandon closer targets.

The Support Enemy creates:

> **The problem of priority.**

---

# Enemy Design Matrix

Each enemy should primarily test a different challenge.

| Enemy          | Primary Problem | Rider Challenge     | Shooter Challenge        |
| -------------- | --------------- | ------------------- | ------------------------ |
| Chaser         | Pressure        | Avoid / ram         | Kill                     |
| Swarm          | Space           | Maintain movement   | Area damage              |
| Ranged Enemy   | Distance        | Close / evade       | Target priority          |
| Blocker        | Pathing         | Find route          | Remove obstacle          |
| Grabber        | Control         | Break free          | Kill quickly             |
| Spitter        | Terrain         | Avoid hazards       | Prioritize threat        |
| Kamikaze       | Timing          | Dodge               | Kill before impact       |
| Leech          | Greed           | Pursue or abandon   | Decide reward value      |
| Drunkard       | Temptation      | Handle consequences | Decide whether to pursue |
| Disruptor      | Adaptation      | Adjust handling     | Remove threat            |
| Shielded Enemy | Positioning     | Create angle        | Aim correctly            |
| Support Enemy  | Priority        | Position team       | Choose target            |

---

# Enemy Combinations

The most interesting difficulty should come from combinations.

A single enemy should be understandable.

Multiple enemies should create complex situations.

---

## Swarm + Ranged Enemy

The Swarm forces the cart to move.

The Ranged Enemy punishes predictable movement.

Result:

> The Rider cannot simply circle around the arena.

---

## Blocker + Chaser

The Blocker prevents escape.

The Chaser creates pressure.

Result:

> The Rider must quickly decide whether to destroy the Blocker or find another route.

---

## Spitter + Swarm

The Spitter reduces available space.

The Swarm occupies the remaining space.

Result:

> The arena gradually becomes dangerous.

---

## Grabber + Ranged Enemy

The Grabber limits movement.

The Ranged Enemy punishes the slowed cart.

Result:

> The Shooter must quickly remove the Grabber.

---

## Drunkard + Disruptor

The Drunkard encourages the team to pursue beer.

The Disruptor makes handling more difficult.

Result:

> The team is tempted to make a dangerous decision.

---

# Enemy Group Design

Enemies should form situations rather than simply spawn individually.

Example:

```text id="3t0x4n"
Ranged Enemy
        ↓
Protected by
        ↓
Swarm
        ↓
While a
        ↓
Grabber
        ↓
Approaches from Behind
```

The team now has multiple problems:

* The Rider must avoid the Grabber
* The Shooter must clear the Swarm
* The Ranged Enemy remains dangerous

The team must communicate.

---

# Enemy Spawning

Enemies should not appear completely randomly.

The spawning system should create:

* Pressure
* Opportunity
* Variety

Possible spawn patterns:

## Front Pressure

Enemies spawn ahead of the cart.

Tests:

* Ramming
* Shooting
* Braking

---

## Side Pressure

Enemies approach from the side.

Tests:

* Turning
* Shooter awareness
* Positioning

---

## Rear Pressure

Enemies chase the cart.

Tests:

* Escape
* Rear-facing attacks
* Momentum

---

## Encirclement

Enemies appear around the cart.

Tests:

* Area damage
* Escape planning
* Emergency abilities

---

# Enemy Density

The number of enemies should be carefully controlled.

The game should create:

> **Controlled chaos.**

Not:

> **Unavoidable visual noise.**

The players should be able to understand:

* What is threatening them
* Where the escape route is
* What target should be killed first

---

# Enemy Telegraphing

Important enemy attacks should be readable.

Examples:

* Flash before an attack
* Visible targeting line
* Warning sound
* Distinct animation
* Clear attack preparation

The player should ideally think:

> **I saw that coming.**

rather than:

> **I had no idea what killed me.**

---

# Enemy Health

Enemies should not simply become bullet sponges.

Difficulty should increase through:

* More enemies
* New behaviors
* Better combinations
* More dangerous positioning

Health increases should be used carefully.

The Shooter should continue to feel powerful.

---

# Enemy Rewards

Different enemies can provide different rewards.

Examples:

## Basic Enemy

* Experience

## Elite Enemy

* Large experience reward
* Beer

## Leech

* Recovers stolen rewards

## Drunkard

* Large beer reward

## Boss

* Major upgrade
* Special reward

This creates target priority decisions.

---

# Elite Enemies

Elite enemies should modify normal enemy behaviors.

Examples:

### Elite Chaser

* Faster
* More health
* Leaves a damaging trail

### Elite Ranged Enemy

* Fires multiple projectiles
* Relocates frequently

### Elite Grabber

* Can grab from farther away

Elites should create:

> **A high-value target that changes the current situation.**

---

# Boss Design

Bosses should test the full team.

A boss should not simply be:

> **A large enemy with a lot of health.**

A good boss should create multiple simultaneous problems.

For example:

```text id="o9m6qn"
Boss Attacks
    ↓
Creates Hazards
    ↓
Summons Enemies
    ↓
Blocks Escape Routes
    ↓
Forces Movement
```

The Rider must:

* Position the cart
* Avoid attacks
* Manage momentum
* Find opportunities

The Shooter must:

* Target weak points
* Manage damage
* Clear summoned enemies
* Choose when to attack the boss

---

# Example Boss Concept — The Store Manager

A possible thematic boss.

## Phase 1

The boss chases the cart.

The Rider must avoid it.

The Shooter attacks.

---

## Phase 2

The boss creates obstacles.

The Rider must navigate around them.

---

## Phase 3

The boss summons smaller enemies.

The Shooter must decide whether to attack the boss or clear the swarm.

---

## Phase 4

The boss becomes faster and more aggressive.

The team must use their build synergy to survive.

The boss should test:

```text id="5c1y6d"
Movement
    +
Target Priority
    +
Positioning
    +
Resource Management
```

---

# Enemy Design Around the Rider

The Rider should be tested by:

* Narrow spaces
* Sudden threats
* Changing terrain
* Momentum challenges
* Escape decisions

Enemies should not constantly make the Rider feel powerless.

The Rider should always have some combination of:

* A route
* A maneuver
* A target
* A risk

---

# Enemy Design Around the Shooter

The Shooter should be tested by:

* Target priority
* Aim
* Range
* Threat evaluation
* Resource management

The Shooter should not simply shoot the closest enemy.

The best target should often be:

> **The enemy that is making the Rider's job hardest.**

---

# Enemy Design Around Cooperation

The best enemies should create disagreements.

Example:

> **Shooter:** "Kill the big guy!"

> **Rider:** "Kill the grabber first!"

> **Shooter:** "I can kill the big guy!"

> **Rider:** "I literally cannot turn!"

This is ideal cooperative tension.

---

# The Enemy Problem Framework

Every enemy should answer:

### What problem does it create?

Examples:

* Space
* Distance
* Control
* Timing
* Greed
* Position
* Priority

### What can the Rider do?

Examples:

* Avoid
* Ram
* Escape
* Reposition
* Use terrain

### What can the Shooter do?

Examples:

* Kill
* Suppress
* Prioritize
* Control
* Protect

### What happens if ignored?

The consequences should be clear.

---

# Enemy Difficulty Formula

Difficulty should preferably come from:

```text id="0k1f1x"
New Threat
    +
New Combination
    +
New Position
    +
New Decision
```

rather than:

```text id="qg0z7v"
More Health
    +
More Damage
```

Numbers can increase, but behavior should be the primary source of complexity.

---

# Recommended Initial Enemy Roster

The first prototype only needs:

## 1. Chaser

Basic pressure.

---

## 2. Ranged Enemy

Forces movement and target priority.

---

## 3. Heavy Enemy

Creates a high-value target.

---

This small roster is enough to test:

```text id="6h2m7w"
Move
    +
Shoot
    +
Prioritize
    +
Escape
```

---

# Recommended Second Wave of Enemies

After the core loop works, add:

## 4. Grabber

Tests control.

---

## 5. Spitter

Tests terrain.

---

## 6. Leech

Tests greed.

These enemies add new decision types rather than simply increasing difficulty.

---

# Enemy Design Success Criteria

The enemy roster is successful if:

```text id="i2q4s8"
Enemies create different problems
        AND
The Rider has meaningful responses
        AND
The Shooter has meaningful target choices
        AND
Enemy combinations create emergent situations
        AND
Threats are readable
        AND
The team can recover from mistakes
```

---

# Final Enemy Design Principle

Enemies should not exist only to be killed.

They should exist to create problems.

The Rider should think:

> **Where can we go?**

The Shooter should think:

> **What needs to die first?**

The team should think:

> **Can we handle this?**

The best enemy encounter should create:

```text id="4af0h1"
A Threat
    ↓
A Decision
    ↓
A Maneuver
    ↓
A Target
    ↓
A Risk
    ↓
A Reward
```

The enemies should force the team to make decisions.

The team should become powerful enough to solve those problems.

Then progression should create new problems that their new power makes possible.

That is the foundation of the game's combat ecosystem.

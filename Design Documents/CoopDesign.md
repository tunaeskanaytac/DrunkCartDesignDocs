# Co-op Design

## Purpose

The game is built around two players sharing one vehicle.

One player controls the cart.

The other player controls the weapon.

This creates a fundamental design challenge:

> **Both players must feel like they are actively playing the game, even though they control different systems.**

The ideal experience is not:

```text
Rider
    ↓
Drives
    ↓
Shooter
    ↓
Plays the Game
```

It should be:

```text
Rider ───────┐
             ├── Shared Survival
Shooter ────┘
```

Both players should have:

* Important decisions
* Moments of mastery
* Personal progression
* Opportunities to make mistakes
* Opportunities to save the team

---

# The Core Co-op Fantasy

The players should feel like:

> **Two idiots trying to operate one increasingly powerful and increasingly uncontrollable machine.**

The cart is the shared body of the team.

```text
Rider
    ↓
Movement

Shooter
    ↓
Combat

Both
    ↓
Survival
```

Neither player should be able to completely succeed alone.

---

# The Core Co-op Relationship

The Rider controls:

> **Where the team is.**

The Shooter controls:

> **What the team kills.**

This creates the fundamental cooperative loop:

```text
Rider Finds Position
        ↓
Shooter Creates Opportunity
        ↓
Rider Moves Again
        ↓
Shooter Prioritizes Threat
        ↓
Team Survives
```

---

# The Most Important Design Principle

The game should not have:

> **A driver and a passenger.**

It should have:

> **A pilot and a gunner.**

Both players should feel responsible for the outcome.

---

# Role Asymmetry

The players should not have identical gameplay.

The asymmetry is a strength.

## Rider

Focuses on:

* Position
* Momentum
* Escape
* Collision
* Route selection
* Vehicle control

## Shooter

Focuses on:

* Aim
* Damage
* Target priority
* Threat removal
* Build specialization

The game becomes interesting because:

> **The players have different information and different priorities.**

---

# The Shared Problem

The best encounters should create a problem that neither player can solve independently.

Example:

```text
Grabber Approaches
        ↓
Rider Begins Losing Control
        +
Ranged Enemy Attacks
        ↓
Shooter Must Kill Grabber
        ↓
Rider Regains Control
```

The Shooter cannot solve the problem without the Rider surviving long enough.

The Rider cannot solve the problem without the Shooter removing the threat.

---

# Player Interdependence

The game should create meaningful dependencies.

## Rider Depends on Shooter

The Shooter must:

* Kill threats
* Clear escape routes
* Protect the cart
* Remove enemies that the Rider cannot safely avoid

---

## Shooter Depends on Rider

The Rider must:

* Create firing angles
* Maintain useful positioning
* Keep the Shooter alive
* Move toward targets
* Avoid making aiming impossible

The goal is:

> **Each player should make the other player better.**

---

# Cooperation Through Positioning

The Rider should not merely move randomly around the arena.

The Rider should actively create opportunities.

Examples:

## Creating a Firing Angle

The Rider positions the cart so the Shooter can attack a vulnerable enemy.

---

## Creating Distance

The Rider moves away from melee enemies so the Shooter can safely attack.

---

## Creating a Collision Opportunity

The Rider lines up a powerful ram while the Shooter clears surrounding enemies.

---

## Creating a Retreat

The Shooter kills the closest threat while the Rider escapes.

---

# The Shooter Should Not Be a Turret

A major danger is that the Shooter becomes:

```text
Aim
    ↓
Hold Fire
    ↓
Win
```

The Shooter should have active decisions.

The Shooter should need to:

* Choose targets
* Manage ammunition or abilities
* React to threats
* Protect the cart
* Decide when to use powerful attacks

The Shooter should constantly ask:

> **What is the most important thing to kill right now?**

---

# The Rider Should Not Be a Taxi

The Rider should not become:

```text
Move Around
        ↓
Wait for Shooter
        ↓
Move Around
```

The Rider should have active gameplay.

The Rider should make decisions about:

* Position
* Momentum
* Ramming
* Escape
* Terrain
* Beer collection
* Risk

The Rider should constantly ask:

> **Where should the cart be right now?**

---

# Shared Target Priority

The two players should often disagree about priorities.

Example:

> **Shooter:** "I'm killing the elite."

> **Rider:** "Kill the Grabber!"

> **Shooter:** "The elite is almost dead!"

> **Rider:** "I cannot steer!"

This is good cooperative tension.

The game should create situations where:

> **There is no obviously correct answer.**

---

# Communication as Gameplay

Communication should provide a real advantage.

Players should naturally communicate:

* Enemy positions
* Threats
* Beer locations
* Escape routes
* Target priorities
* Upcoming abilities

Example:

> **Rider:** "I'm turning left."

> **Shooter:** "I need the enemy on the right."

> **Rider:** "I can't get you an angle yet."

> **Shooter:** "Then ram the front one."

This should emerge from the mechanics rather than requiring a communication system.

---

# Information Asymmetry

The two players should not necessarily see exactly the same thing.

The Rider may have better awareness of:

* Terrain
* Obstacles
* Movement
* Escape routes

The Shooter may have better awareness of:

* Enemy health
* Weak points
* Threats
* Target opportunities

This creates communication.

The players should need to tell each other things.

---

# The Shared Camera Problem

A major design question is camera perspective.

Possible approaches:

## Single Shared Camera

Both players see the same world.

### Advantages

* Simple
* Easy to understand
* Strong sense of being on one vehicle

### Disadvantages

* The Shooter may struggle to see targets
* The Rider may not have enough spatial awareness

This is probably the best starting point.

---

## Different Views

Each player receives a different camera.

### Rider

Third-person or top-down driving view.

### Shooter

Aiming-focused view.

This provides stronger role distinction.

However, it increases:

* Technical complexity
* Visual complexity
* Potential confusion

---

## Shared World, Different UI

Both players use the same camera but receive different information.

For example:

### Rider UI

* Cart speed
* Momentum
* Handling
* Nearby obstacles

### Shooter UI

* Enemy health
* Target information
* Weapon cooldowns

This is likely a good compromise.

---

# Player Death

Player death should be carefully designed.

The game should avoid:

> **One player dying and waiting for twenty minutes.**

Possible solutions:

## Downed State

A player becomes incapacitated.

The other player can revive them.

---

## Shared Cart Health

The cart is the primary health pool.

Players can be injured without immediately ending the run.

---

## Temporary Separation

A player can be ejected from the cart.

The Rider must recover them.

This could create a funny emergency situation.

---

# Recommended Initial Death System

The simplest version:

```text
Player Takes Too Much Damage
        ↓
Player Becomes Downed
        ↓
Other Player Can Revive
        ↓
Revival Succeeds
        or
        ↓
Team Fails
```

The downed player should still have limited interaction.

For example:

* Shoot weakly
* Mark enemies
* Crawl toward the cart
* Use a last ability

This prevents the player from becoming completely passive.

---

# Ejection as a Gameplay Mechanic

The shopping cart concept makes player ejection especially interesting.

Possible events:

* Collision launches the Shooter out
* A powerful attack knocks a player off
* The Rider loses control
* The cart flips

The ejected player could:

```text
Land
    ↓
Survive
    ↓
Fight Temporarily
    ↓
Return to Cart
```

This creates a unique co-op problem:

> **The team is temporarily separated.**

The Rider must decide whether to:

* Go back
* Keep moving
* Clear enemies first

The Shooter must decide whether to:

* Fight
* Run
* Reach the cart

---

# Ejection Should Be Used Carefully

If ejection happens constantly:

> **It becomes annoying.**

If it happens occasionally:

> **It becomes memorable.**

The player should usually understand why it happened.

---

# Shared Health vs Individual Health

The game can use:

## Shared Cart Health

The cart has one health bar.

### Advantages

* Simple
* Strong shared identity
* Easy to understand

### Disadvantages

* Individual mistakes affect everyone equally

---

## Individual Player Health

Each player has their own health.

### Advantages

* More personal responsibility
* More room for individual mistakes

### Disadvantages

* More complicated

---

## Recommended Hybrid

Use:

```text
Player Health
        +
Cart Health
```

The cart is the main survival resource.

Players can be individually downed.

This creates multiple failure states.

---

# The Cart as the Shared Body

The cart should represent the team's shared condition.

Possible states:

```text
Healthy Cart
    ↓
Damaged Cart
    ↓
Critical Cart
    ↓
Destroyed Cart
```

The players should feel:

> **The cart is our shared life.**

---

# Cooperative Upgrades

Some upgrades should benefit one player.

Others should benefit both.

Some should create tradeoffs.

---

## Rider Upgrade

> Increased acceleration.

Directly improves Rider gameplay.

---

## Shooter Upgrade

> Additional projectile.

Directly improves Shooter gameplay.

---

## Shared Upgrade

> Beer increases maximum cart speed.

Benefits the entire team.

---

## Tradeoff Upgrade

> More Shooter damage, less cart handling.

Creates a team decision.

---

# Role-Specific Builds

The players should be able to develop distinct identities.

## Rider Build

Focuses on:

* Speed
* Collision
* Handling
* Defense
* Beer collection

---

## Shooter Build

Focuses on:

* Damage
* Fire rate
* Critical hits
* Area attacks
* Target control

---

## Team Build

Focuses on:

* Synergy
* Shared bonuses
* Beer
* Coordination

---

# Build Conflict

Some upgrades should create tension.

Example:

> **Shooter Upgrade:** More damage at high intoxication.

> **Rider Upgrade:** Better handling while sober.

The team must decide:

> **Do we want more power or more control?**

This should be a recurring theme.

---

# Cooperative Upgrade Choices

Some choices should be made together.

For example:

```text
Upgrade Options:
    ↓
Rider Upgrade
Shooter Upgrade
Team Upgrade
```

The team discusses:

> **Who needs the upgrade more?**

This creates shared ownership of the build.

---

# Individual Upgrade Choices

Other upgrades can be chosen separately.

For example:

```text
Rider Chooses
    ↓
Rider Upgrade

Shooter Chooses
    ↓
Shooter Upgrade
```

This reduces arguments over every single upgrade.

The best system is probably a combination of both.

---

# The "Who Gets the Beer?" Problem

Beer creates an important cooperative decision.

Possible options:

## Shooter Always Drinks

Simple.

The Rider experiences the consequences.

---

## Either Player Can Drink

Creates more strategic possibilities.

The Rider could potentially drink to gain driving benefits.

---

## Shared Beer Resource

The team chooses how to use it.

This is the most cooperative option.

---

# Recommended Beer Structure

Initially:

```text
Beer
    ↓
Shared Resource
    ↓
Team Decides Whether to Consume
```

Consumption primarily affects the Shooter's power.

Intoxication affects the cart.

This creates a natural shared decision.

---

# Co-op Resource Management

The team should have resources that both players care about.

Examples:

* Beer
* Healing
* Special abilities
* Cart repairs
* Ultimate charge

The players should regularly discuss:

> **Who should use this?**

---

# Cooperative Abilities

Some abilities should require both players.

Examples:

## Boost Ram

The Rider activates the boost.

The Shooter marks a target.

Together:

```text
Mark Target
    ↓
Charge
    ↓
Massive Impact
```

---

## Emergency Escape

The Rider activates a maneuver.

The Shooter clears enemies behind the cart.

---

## Combined Ultimate

The Rider creates momentum.

The Shooter fires a powerful attack.

The result is a team attack.

These abilities reward coordination.

---

# Cooperative Combos

The game should support simple combinations.

Example:

```text
Rider:
High-Speed Charge
        +
Shooter:
Explosive Shot
        ↓
Massive Area Damage
```

Or:

```text
Rider:
Drift Around Enemies
        +
Shooter:
Area Weapon
        ↓
Enemies Gathered Together
        ↓
Large Damage
```

The players should discover combinations naturally.

---

# Rider and Shooter Skill Expression

Both roles need skill ceilings.

## Rider Skill

The Rider improves at:

* Maintaining momentum
* Braking
* Drifting
* Dodging
* Ramming
* Positioning

---

## Shooter Skill

The Shooter improves at:

* Aiming
* Target selection
* Timing abilities
* Predicting movement
* Managing cooldowns

The game should reward practice for both players.

---

# The Rider's Fun Problem

The Rider's gameplay should not be:

> **Avoid everything.**

The Rider should actively interact with enemies.

Possible actions:

* Ram
* Drift
* Boost
* Push
* Knock enemies away
* Collect beer
* Create firing angles

The Rider should feel like a combat participant.

---

# The Shooter's Fun Problem

The Shooter's gameplay should not be:

> **Shoot the nearest enemy.**

The Shooter should:

* Identify the most dangerous enemy
* Protect the Rider
* Choose when to use abilities
* Create kill opportunities
* Manage resources

The Shooter should feel responsible for the team's survival.

---

# Cooperative Failure

Mistakes should be shared experiences.

Examples:

## Rider Mistake

The Rider crashes into an obstacle.

The Shooter loses their firing position.

---

## Shooter Mistake

The Shooter ignores a Grabber.

The Rider loses control.

---

## Shared Mistake

The team drinks too much beer.

The cart becomes uncontrollable.

These moments should be funny rather than frustrating whenever possible.

---

# Blame and Recovery

The game should avoid making mistakes feel like:

> **"You ruined the run."**

Instead, mistakes should create:

> **"Oh no. How do we recover from this?"**

The team should have recovery tools.

Examples:

* Emergency boost
* Defensive ability
* Revive
* Temporary invulnerability
* Escape route

---

# Co-op Difficulty

The game should not simply multiply enemy health for two players.

The difficulty should come from:

* More complex situations
* More simultaneous threats
* Greater communication requirements

The team should feel stronger because there are two players.

But the game should challenge:

> **Their ability to cooperate.**

---

# Player Skill Mismatch

A common problem:

> One player is much better than the other.

The game should accommodate this.

The more experienced player should be able to:

* Help the other player
* Create opportunities
* Recover from mistakes

The less experienced player should still:

* Have meaningful actions
* Feel useful
* Improve over time

---

# Asymmetric Skill Levels

The Rider and Shooter should have different skill curves.

A new player might:

* Drive safely but slowly
* Shoot basic enemies effectively

An experienced player might:

* Drift through enemy groups
* Make aggressive positioning decisions
* Prioritize threats perfectly

The game should allow both players to contribute at different skill levels.

---

# The Passenger Problem

The Shooter should never feel like:

> **A passenger waiting for the Rider to drive somewhere.**

The Rider should never feel like:

> **A chauffeur delivering the Shooter to targets.**

Both players should constantly be making decisions.

---

# Activity Balance

The gameplay should alternate responsibilities.

Example:

```text
Rider Is Active
        ↓
Shooter Is Active
        ↓
Both Are Active
        ↓
Rider Creates Opportunity
        ↓
Shooter Exploits Opportunity
```

The roles can have different intensity levels.

They should not both need maximum concentration every second.

---

# Cooperative Moments

The game should deliberately create moments where both players are essential.

Examples:

## The Escape

Rider finds the route.

Shooter clears the path.

---

## The Elite

Rider positions the cart.

Shooter kills the target.

---

## The Beer Run

Rider reaches the beer.

Shooter protects the cart.

---

## The Boss

Rider survives the arena.

Shooter manages damage.

---

# The Best Co-op Moments

The best moments should sound like:

> **"I have an idea."**

> **"Do it."**

> **"Wait, wait, wait—"**

> **"I got it!"**

> **"I did not get it."**

> **"Why did you drink that?"**

> **"Because it was there."**

This is the emotional identity the game should aim for.

---

# Recommended Initial Co-op Prototype

The first playable co-op version should include:

## Rider

* Drive
* Brake
* Turn
* Ram

## Shooter

* Aim
* Shoot
* Basic ability

## Shared

* Enemy health
* Cart health
* Beer
* Intoxication

## Cooperation

* Rider positioning affects shooting
* Shooter kills threats to protect Rider
* Beer changes both roles

This is enough to test the core fantasy.

---

# Co-op Playtest Questions

### Rider

* Does driving feel like a real game?
* Do I have meaningful decisions?
* Can I actively fight enemies?

### Shooter

* Do I have enough to do?
* Do I need the Rider's positioning?
* Do I feel responsible for protecting the team?

### Cooperation

* Do we communicate naturally?
* Do we disagree about decisions?
* Does cooperation improve performance?

### Fun

* Are our failures funny?
* Do we have memorable moments?
* Would we want to play another run?

---

# Co-op Success Criteria

The co-op system is successful if:

```text
The Rider has meaningful gameplay
        AND
The Shooter has meaningful gameplay
        AND
Neither player can completely replace the other
        AND
Both players make important decisions
        AND
Communication improves performance
        AND
Mistakes create memorable moments
        AND
The team can recover from failure
```

---

# Final Co-op Design Principle

The game should not be about:

> **One player driving while the other player shoots.**

It should be about:

> **Two players trying to coordinate a single chaotic machine while disagreeing about what to do with it.**

The Rider asks:

> **Where are we going?**

The Shooter asks:

> **What are we killing?**

The beer asks:

> **How much worse can we make this?**

The best possible co-op moment is when all three questions collide.

```text
Rider:
"We need to leave."

Shooter:
"There's beer over there."

Rider:
"We are being chased."

Shooter:
"One more beer."

Rider:
"Absolutely not."

Shooter:
"Too late."
```

That is the kind of interaction that can make the game feel like a genuine **friendslop game** rather than a standard roguelike with a multiplayer mode.

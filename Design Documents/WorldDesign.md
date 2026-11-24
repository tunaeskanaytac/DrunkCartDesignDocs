# World and Level Design

## Purpose

The level is not merely a place where enemies spawn.

The level is part of the gameplay.

The Rider interacts with:

* Terrain
* Obstacles
* Ramps
* Hazards
* Narrow passages
* Open spaces
* Destructible objects
* Beer locations

The environment should create opportunities for:

```text
Movement
    +
Combat
    +
Risk
    +
Positioning
```

The core design principle is:

> **The Rider should have interesting decisions even when there are no enemies directly in front of the cart.**

---

# The World Fantasy

The world should support the central fantasy:

> **Two friends are driving an increasingly unstable shopping cart through increasingly absurd environments while fighting everything in their way.**

The world should feel:

* Chaotic
* Physical
* Interactive
* Slightly ridiculous
* Dangerous in entertaining ways

The environment should feel like something the players can use.

---

# The Level Is a Weapon

The Shooter has a weapon.

The Rider should also have a weapon.

That weapon is:

> **The environment.**

The Rider should be able to use:

* Momentum
* Walls
* Ramps
* Obstacles
* Narrow paths
* Environmental hazards

The Rider should be thinking:

> **Can I use this part of the map?**

---

# Basic Arena Structure

The game should avoid making every arena a featureless circle.

A useful arena should contain:

```text
Open Space
    +
Constrained Space
    +
Dangerous Space
    +
Reward Space
```

For example:

```text
             Beer
              ●
              │
    ┌─────────┴─────────┐
    │                   │
    │    Open Arena     │
    │                   │
    │  ┌─────┐   ┌───┐  │
    │  │Ramp │   │Wall│  │
    │  └─────┘   └───┘  │
    │                   │
    └───────┬───────────┘
            │
       Narrow Route
```

The Rider should constantly evaluate:

> **Where do we want to be?**

---

# The Three Types of Space

## Open Space

Useful for:

* High-speed movement
* Dodging
* Ramming
* Kiting enemies

The Rider has freedom.

The danger is:

> **Enemies can approach from every direction.**

---

## Constrained Space

Useful for:

* Creating chokepoints
* Controlling enemy approach
* Using walls
* Making positioning important

The danger is:

> **The cart has less room to maneuver.**

---

## Dangerous Space

Contains:

* Hazards
* Cliffs
* Explosives
* Traps
* Environmental damage

The danger is obvious.

The reward should justify entering it.

---

# Arena Flow

An arena should have a recognizable flow.

```text
Enter Area
    ↓
Explore
    ↓
Encounter Threat
    ↓
Move Through Space
    ↓
Collect Rewards
    ↓
Reach New Area
```

The team should not simply stand in the center and wait for enemies.

---

# Movement Should Have Purpose

The Rider should move because:

* A threat is approaching
* A target is vulnerable
* Beer is nearby
* A better position exists
* The current area is becoming dangerous
* A new route has opened

Movement should be a decision.

Not just:

> **Hold forward and circle around the enemies.**

---

# Arena Layout Principles

Every arena should ideally contain:

## A Safe Area

A place where the team can recover briefly.

---

## A High-Risk Area

A dangerous place with better rewards.

---

## A Movement Feature

Something that makes driving interesting.

Examples:

* Ramp
* Slope
* Narrow corridor
* Destructible barrier

---

## A Landmark

A recognizable object or structure.

This helps players understand where they are.

---

# Momentum Spaces

Some areas should reward maintaining speed.

Examples:

* Long corridors
* Downhill paths
* Wide open roads

These allow the Rider to build momentum.

The Rider can then:

```text
Accelerate
    ↓
Build Momentum
    ↓
Choose Target
    ↓
Ram
```

---

# Braking Spaces

Other areas should test stopping and control.

Examples:

* Sharp turns
* Narrow corners
* Obstacles
* Dead ends

The Rider must plan ahead.

This is particularly important when intoxication increases momentum.

---

# Turning Spaces

Some areas should reward precise steering.

Examples:

* Slalom obstacles
* Curved paths
* Interconnected routes

These can test Rider skill without requiring combat.

---

# Ramps

Ramps are one of the most important possible level features.

They can provide:

* Vertical movement
* Momentum
* Shortcuts
* Evasion
* Collision opportunities

A ramp should not exist merely for visual decoration.

The Rider should be able to ask:

> **Should I take the ramp?**

---

# Ramp Design

A ramp can create a choice:

```text
Normal Route
    ↓
Safer
    ↓
Lower Reward
```

or:

```text
Ramp
    ↓
Risky Jump
    ↓
Higher Reward
```

The Rider chooses.

---

# Jumping

Jumping should have a purpose.

Possible benefits:

* Avoid ground hazards
* Cross gaps
* Escape enemies
* Reach beer
* Perform an aerial ram

The player should not be required to perform precise platforming constantly.

The game is primarily a combat roguelike.

The vehicle physics should remain the focus.

---

# Aerial Combat

The Shooter should still be able to act while airborne.

This creates interesting moments.

```text
Ramp
    ↓
Cart Becomes Airborne
    ↓
Rider Controls Landing
    +
Shooter Fires During Jump
```

This can create memorable cooperative moments.

---

# Landing

Landing should feel physical.

Possible outcomes:

## Good Landing

* Maintain momentum
* Continue moving

---

## Bad Landing

* Lose speed
* Spin
* Take damage
* Eject a player

The result should depend on the situation.

---

# Obstacles

Obstacles should create decisions.

Examples:

* Concrete barriers
* Shopping shelves
* Cars
* Crates
* Fallen objects

The Rider should be able to:

* Avoid them
* Ram them
* Go around them
* Use them as cover

---

# Destructible Obstacles

Destruction is especially valuable because it allows the Rider to create routes.

For example:

```text
Blocked Path
    ↓
Ram Barrier
    ↓
New Route Opens
```

This makes the Rider feel powerful.

---

# Destructible Objects

Possible objects:

* Wooden crates
* Fences
* Barricades
* Weak walls
* Vehicles

Different objects can have different collision properties.

---

# Destruction and the Shooter

The Shooter should also be able to destroy obstacles.

This creates role interaction.

Example:

```text
Rider:
Cannot safely ram the barricade

Shooter:
Destroys the barricade

Rider:
Uses the new route
```

The players solve the environment together.

---

# Environmental Hazards

Hazards should create movement decisions.

Examples:

* Fire
* Oil
* Acid
* Electricity
* Explosive barrels
* Falling objects

The Rider must decide:

> **Do we go around or through?**

---

# Oil

Oil can create reduced traction.

This is particularly interesting because it interacts with intoxication.

```text
Drunk Cart
    +
Oil
    ↓
Extremely Difficult Handling
```

This should be used carefully.

The combination could be:

> **Terrible.**

Which is potentially:

> **Extremely funny.**

---

# Fire

Fire can:

* Damage the cart
* Create temporary zones
* Ignite objects

The Rider must avoid the area.

The Shooter may be able to extinguish or destroy its source.

---

# Explosives

Explosive objects can be used offensively.

The Rider may:

* Ram them
* Push them toward enemies

The Shooter may:

* Shoot them from a distance

This creates cooperative environmental combat.

---

# Enemy and Environment Interaction

Enemies should interact with the environment.

Examples:

## Enemy Pushed Into Hazard

```text
Rider
    ↓
Rams Enemy
    ↓
Enemy Hits Fire
    ↓
Enemy Takes Damage
```

---

## Enemy Blocks Route

```text
Heavy Enemy
    ↓
Blocks Narrow Path
    ↓
Rider Must:
Ram
or
Shooter Must:
Kill
```

---

## Enemy Creates Hazard

```text
Spitter
    ↓
Creates Acid
    ↓
Available Space Shrinks
```

The environment should make enemy encounters more complex.

---

# The Environment as a Battlefield

The team should learn to understand spaces.

For example:

> **"This is the good ramming area."**

> **"Don't go into the oil."**

> **"Take the left route. There's a ramp."**

> **"The narrow corridor is bad when we're drunk."**

The players should develop spatial knowledge.

---

# Beer Locations

Beer should be placed intentionally.

Beer should sometimes appear:

* In open spaces
* Behind obstacles
* Near hazards
* At the end of dangerous routes

The team should need to decide:

> **How much do we want this beer?**

---

# Beer as a Level Objective

The level can create explicit beer opportunities.

Example:

```text
Beer Crate
    ↓
Surrounded by Enemies
    ↓
Team Decides
    ↓
Take Risk
    or
Leave It
```

This makes beer part of the world.

---

# Reward Locations

The same principles should apply to other rewards.

Possible reward locations:

## Safe Reward

Easy to collect.

Small reward.

---

## Dangerous Reward

Difficult to reach.

Large reward.

---

## Hidden Reward

Requires exploration.

Special reward.

---

# Level Geometry and the Rider

The Rider's control system should be designed around level geometry.

The level should provide opportunities for:

* Braking
* Turning
* Drifting
* Acceleration
* Ramming
* Jumping

If the level is entirely open:

> **Only acceleration and turning matter.**

If the level is too cramped:

> **The cart feels frustrating rather than skillful.**

The level needs a mixture.

---

# The Recommended Geometry Ratio

A starting hypothesis:

```text
50%
Open Space

25%
Constrained Routes

15%
Hazards

10%
Special Movement Features
```

These values are not rules.

They are a starting point for prototyping.

The most important thing is variety.

---

# Route Design

The team should have multiple ways to move through an area.

Example:

```text
            ┌── Dangerous Route ── Reward
            │
Start ──────┤
            │
            └── Safe Route ─────── Normal Progression
```

The team chooses its risk.

---

# Route Choice

Different routes should offer different advantages.

## Wide Route

* Easy to control
* More enemies

## Narrow Route

* Fewer enemies
* Difficult to maneuver

## Dangerous Route

* Environmental hazards
* Better rewards

This creates meaningful navigation.

---

# Arena Transitions

Moving between areas should be part of the gameplay.

Possible transitions:

* Open gates
* Break barriers
* Survive a wave
* Defeat an elite
* Reach a destination

The team should feel like they are progressing through a place.

---

# The Level Should Not Be a Corridor

The game should not become:

```text
Room
    ↓
Fight
    ↓
Corridor
    ↓
Fight
    ↓
Room
```

This makes the Rider feel like they are moving between combat encounters.

Instead:

```text
Area
    ↓
Movement Choice
    ↓
Combat
    ↓
Environmental Interaction
    ↓
Reward Choice
    ↓
New Area
```

The movement itself should be gameplay.

---

# World Themes

The game can use environments that naturally support vehicle gameplay.

Possible themes:

## Supermarket

The obvious starting environment.

Features:

* Shopping aisles
* Shelves
* Escalators
* Shopping carts
* Warehouse sections
* Parking lot

This is probably the strongest initial setting.

---

## Parking Lot

Features:

* Cars
* Open space
* Speed
* Ramps
* Traffic

Good for:

> **High-speed driving.**

---

## Industrial Area

Features:

* Pipes
* Conveyors
* Hazards
* Narrow routes

Good for:

> **Environmental danger.**

---

## Construction Site

Features:

* Ramps
* Gaps
* Cranes
* Destructible barriers

Good for:

> **Vertical movement.**

---

## Amusement Park

Features:

* Rides
* Tracks
* Curved routes
* Moving obstacles

Good for:

> **Unusual movement.**

---

# Recommended Initial World

The first complete prototype should probably take place in:

> **A supermarket and its surrounding parking lot.**

This immediately supports the game's identity.

Possible progression:

```text
Store Interior
    ↓
Warehouse
    ↓
Loading Area
    ↓
Parking Lot
    ↓
Final Encounter
```

The environment can naturally become larger and more chaotic.

---

# Supermarket Level Structure

## Aisles

Narrow routes.

The Rider must control the cart carefully.

---

## Main Floor

Open space.

Good for:

* Combat
* Ramming
* Enemy swarms

---

## Checkout Area

Creates:

* Narrow lanes
* Obstacles
* Destructible objects

---

## Warehouse

Large objects.

Heavy enemies.

Environmental hazards.

---

## Loading Dock

Large open space.

Vehicles.

Ramps.

---

## Parking Lot

Maximum speed.

Large enemy encounters.

Final escape sequence.

---

# Thematic Interaction

The environment should be funny because it is recognizable.

Examples:

* The cart crashes through a supermarket display
* Beer is located in the beer aisle
* The team destroys a checkout
* Enemies attack from behind shelves
* The cart launches off a loading ramp

The world should support the game's comedic identity.

---

# Level Design and Camera

The camera should make movement readable.

The Rider needs to see:

* Upcoming obstacles
* Turns
* Hazards
* Routes

The Shooter needs to see:

* Enemies
* Targets
* Projectiles

The camera should prioritize gameplay readability over cinematic presentation.

---

# Camera Problems to Avoid

Avoid:

* Excessive camera shake
* Unreadable walls
* Sudden blind corners
* Enemies appearing directly behind the cart
* Excessive visual effects

Especially because:

> **The beer system already creates visual and control chaos.**

The level should not add unnecessary confusion.

---

# Level Difficulty

Difficulty should increase through:

## More Complex Geometry

More routes and hazards.

---

## More Enemy Interaction

Enemies use the environment.

---

## More Pressure

Less safe space.

---

## More Consequences

Mistakes become more dangerous.

The level should not simply become smaller.

---

# Intoxication and Level Design

The level should change in difficulty depending on intoxication.

A route that is easy while sober may become difficult while drunk.

For example:

```text
Sober
    ↓
Narrow Turn
    ↓
Easy
```

But:

```text
Drunk
    ↓
Narrow Turn
    ↓
Difficult
```

This makes the environment interact directly with the beer system.

---

# Intoxication-Specific Opportunities

High intoxication could also create advantages.

For example:

```text
Drunk
    ↓
High Momentum
    ↓
Jump Ramp
    ↓
Reach Secret Area
```

The same mechanic that creates danger can create opportunities.

This is important.

Beer should not only make the level harder.

It should change how the level is played.

---

# The Environment Should Reward Mastery

A skilled Rider should eventually be able to:

* Take dangerous shortcuts
* Maintain speed through corners
* Use ramps effectively
* Ram enemies into hazards
* Navigate while intoxicated

The level should have a skill ceiling.

The player should improve from:

> **"I can barely drive this thing."**

to:

> **"I know exactly how to use this momentum."**

---

# Level-Specific Mechanics

Different levels should eventually have their own rules.

Examples:

## Supermarket

* Destructible shelves
* Narrow aisles
* Shopping obstacles

## Parking Lot

* Cars
* Large open spaces
* High speeds

## Construction Site

* Gaps
* Ramps
* Falling objects

Each level should change the Rider's priorities.

---

# Procedural vs Handcrafted Levels

The game could use:

## Handcrafted Arenas

### Advantages

* Better designed movement challenges
* More memorable spaces
* Better control over pacing

### Disadvantages

* Less replayability

---

## Procedural Arenas

### Advantages

* More replayability
* More variety

### Disadvantages

* Potentially poor vehicle routes
* Less intentional design

---

# Recommended Approach

Use:

> **Handcrafted gameplay modules with procedural or semi-randomized arrangement.**

For example:

```text
Arena Module
    ↓
Route Module
    ↓
Hazard Module
    ↓
Reward Module
    ↓
Arena Module
```

This provides replayability while preserving designed gameplay.

---

# Example Run Layout

```text
[Supermarket Entrance]
        ↓
[Open Main Floor]
        ↓
     ┌──┴──┐
     ↓     ↓
[Beer]  [Elite]
     └──┬──┘
        ↓
[Checkout Area]
        ↓
[Warehouse]
        ↓
     ┌──┴──┐
     ↓     ↓
[Safe] [Dangerous]
     └──┬──┘
        ↓
[Loading Dock]
        ↓
[Parking Lot]
        ↓
[Final Encounter]
```

The team makes decisions along the way.

---

# The Level Design Test

For every area, ask:

### What does the Rider do here?

If the answer is only:

> **Drive forward.**

The area needs more design.

---

### What does the Shooter do here?

If the answer is only:

> **Shoot enemies.**

The area may need environmental interactions.

---

### What decision does the team make?

Every major area should ideally create a choice.

Examples:

* Safe or dangerous route?
* Beer or safety?
* Speed or control?
* Fight or escape?
* Open area or narrow shortcut?

---

# Prototype Level

The first level prototype should be extremely small.

It only needs:

```text
Start
    ↓
Open Arena
    ↓
Narrow Route
    ↓
Ramp
    ↓
Reward Area
    ↓
Enemy Arena
    ↓
Exit
```

This is enough to test whether:

* Driving is fun
* Momentum is interesting
* The Shooter can aim while moving
* The environment creates meaningful decisions

---

# World and Level Design Success Criteria

The level design is successful if:

```text
The Rider has meaningful movement decisions
        AND
The Shooter benefits from good positioning
        AND
The environment can be used offensively
        AND
Different areas create different movement challenges
        AND
Rewards create spatial decisions
        AND
Beer interacts with the environment
        AND
The level remains readable during chaos
```

---

# Final World Design Principle

The world should not be:

> **A place where the game happens.**

It should be:

> **One of the things the players are playing.**

The ideal encounter looks like:

```text
Enemy Horde
    +
Narrow Corridor
    +
Beer Reward
    +
Ramp
    +
High Intoxication
```

The team must decide:

> **Do we take the beer, go through the corridor, launch off the ramp, and hope we can still control the cart when we land?**

The answer should frequently be:

> **Yes.**

That is the kind of level design that can turn the shopping cart from a gimmick into the actual core of the game.

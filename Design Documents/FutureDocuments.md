You have enough design documentation for the **core concept and first prototype**. I would avoid writing more documents right now and start building. In the future, these are the documents I would consider useful:

## Highest Priority

### `playtest-plan.md`

How to test the prototype systematically.

Would cover:

* What to test
* Which questions each playtest should answer
* Metrics to track
* How to identify whether Rider or Shooter is less fun
* When to rework a system versus add content

This should probably be the **next document after the first playable prototype**.

---

### `technical-architecture.md`

The actual structure of the game's code and systems.

Would cover:

* Game states
* Run management
* Player architecture
* Cart architecture
* Combat architecture
* Event systems
* Data-driven systems
* Save data

Your current `technical-prototype-plan.md` is about **what to build**. This would be about **how the finished game should be structured**.

---

### `networking-design.md`

Important if you commit to online multiplayer.

Would cover:

* Network architecture
* Authority model
* Cart movement synchronization
* Player input synchronization
* Enemy synchronization
* Physics replication
* Host migration
* Reconnection
* Lag compensation

I would **not** write this yet. Network architecture should be informed by the actual prototype.

---

## Gameplay Systems

### `weapon-design.md`

The Shooter's weapons and weapon archetypes.

Possible categories:

* Automatic weapons
* Shotguns
* Explosives
* Beam weapons
* Homing weapons
* High-risk weapons

This should come after the basic Shooter prototype proves that aiming and shooting are fun.

---

### `ability-design.md`

Active abilities for both players.

For example:

**Rider:**

* Boost
* Drift
* Ram
* Emergency brake
* Defensive maneuver

**Shooter:**

* Grenade
* Turret
* Area attack
* Marking
* Crowd control

**Co-op:**

* Combined abilities

---

### `item-and-upgrade-design.md`

The actual upgrade pool.

Would define:

* Rider upgrades
* Shooter upgrades
* Shared upgrades
* Beer upgrades
* Synergies
* Upgrade rarity
* Upgrade categories

This is probably more useful than writing a huge upgrade list immediately.

---

### `boss-design.md`

Bosses should specifically test the game's two-player structure.

A good boss should create problems for both players.

For example:

* The Rider must navigate a dangerous arena
* The Shooter must target weak points
* The team must coordinate movement and attacks

---

### `event-design.md`

Non-combat events during a run.

Examples:

* Beer-related events
* Risk/reward choices
* Shops
* Repair stations
* Strange NPCs
* Gambling-style decisions
* Environmental challenges

This would help the game feel like a roguelike rather than simply:

> Fight → Upgrade → Fight → Upgrade.

---

## Content Design

### `enemy-roster.md`

A complete overview of enemy roles and how they interact.

The existing `enemy-design.md` defines the philosophy. This future document would contain the actual roster:

| Enemy        | Role     | Threat             | Rider Interaction | Shooter Interaction |
| ------------ | -------- | ------------------ | ----------------- | ------------------- |
| Basic Enemy  | Pressure | Contact damage     | Avoid / ram       | Kill                |
| Grabber      | Control  | Disables cart      | Escape            | Prioritize          |
| Ranged Enemy | Zoning   | Projectile attacks | Keep moving       | Kill                |
| Tank         | Blocker  | Controls space     | Ram / avoid       | Weak-point attack   |

---

### `world-progression.md`

How the game progresses from one environment to another.

For example:

```text
Supermarket
    ↓
Warehouse
    ↓
Parking Lot
    ↓
Industrial Area
    ↓
??? 
```

Would define:

* World themes
* Mechanical identity of each world
* Enemy pools
* Environmental hazards
* Bosses
* Beer-related features

---

### `procedural-generation-design.md`

Only if you decide procedural generation is worth the complexity.

Would define:

* Arena modules
* Room connections
* Route generation
* Reward placement
* Enemy encounter generation
* Ensuring cart-friendly layouts

I would strongly recommend waiting until you have handcrafted levels that are fun.

---

### `encounter-design.md`

How individual combat encounters are constructed.

For example:

```text
Encounter Type:
    Enemy Horde
    + Narrow Route
    + Beer Reward
    + Ranged Pressure
```

This is useful for creating variety without needing hundreds of enemy types.

---

## Progression and Replayability

### `meta-progression-design.md`

Permanent progression between runs.

For example:

* Unlocking new weapons
* Unlocking new characters
* Unlocking new cart parts
* New beer types
* New worlds

However, be careful here. Meta-progression can easily make the game feel like it requires grinding.

---

### `character-design.md`

If the game eventually has multiple Riders and Shooters.

For example:

* Different Rider characters
* Different Shooter characters
* Unique abilities
* Different starting stats

This could add replayability, but I would not assume the game needs character classes yet.

---

### `cart-customization-design.md`

A potentially very important future system.

The shopping cart could have customizable parts:

* Wheels
* Frame
* Engine
* Seat
* Weapon mount
* Beer storage

This could be a particularly good way to give the Rider progression without simply adding generic stat upgrades.

Example:

```text
Better Wheels
    ↓
Improved Handling

Bigger Engine
    ↓
More Speed

Reinforced Frame
    ↓
Better Ramming

Beer Cooler
    ↓
More Beer Capacity
```

This feels thematically stronger than generic equipment.

---

### `build-synergy-design.md`

This would document the game's major build archetypes.

Examples:

#### Drunken Berserker

```text
High Intoxication
+
High Speed
+
Ram Damage
```

#### Gun Platform

```text
Stable Cart
+
High Shooter Damage
+
Long Range
```

#### Chaos Build

```text
High Intoxication
+
Random Effects
+
Unpredictable Movement
```

This document becomes useful once you have enough upgrades to create actual build diversity.

---

## Presentation and Production

### `art-direction.md`

The visual identity of the game.

Would define:

* Art style
* Color palette
* Character design
* Cart design
* Enemy silhouettes
* VFX style
* UI style

---

### `audio-design.md`

Audio is especially important for a chaotic friendslop game.

Would cover:

* Cart sounds
* Wheel sounds
* Collision sounds
* Beer sounds
* Intoxication audio
* Weapon sounds
* Enemy sounds
* Music progression

The cart should probably sound funny and increasingly broken as it becomes more intoxicated.

---

### `ui-ux-design.md`

Would define:

* Shared UI
* Rider-specific UI
* Shooter-specific UI
* Intoxication meter
* Beer inventory
* Upgrade selection
* Multiplayer readability

The UI needs to clearly communicate information to two players without cluttering the screen.

---

### `accessibility-design.md`

Especially useful for:

* Camera shake
* Screen sway
* Motion effects
* Colorblindness
* Input remapping
* Controller support
* Seizure-sensitive effects

This game has a particularly strong reason to provide options for camera and screen effects because intoxication is one of the core mechanics.

---

## Eventually

### `production-roadmap.md`

The actual development plan from prototype to release.

```text
Prototype
    ↓
Vertical Slice
    ↓
Alpha
    ↓
Beta
    ↓
Early Access / Release
```

---

### `monetization-design.md`

Only when you know the game is actually going to be released.

---

### `marketing-and-store-page.md`

Steam page, trailer, screenshots, and the game's elevator pitch.

---

### `qa-test-plan.md`

Testing:

* Multiplayer edge cases
* Physics bugs
* Network issues
* Progression bugs
* Softlocks
* Crashes

---

# My Recommended Long-Term Document Structure

If this project grows, I would organize the documents like this:

```text
design/
│
├── 00-vision/
│   ├── ideas.md
│   ├── core-loop.md
│   └── game-pillars.md
│
├── 01-gameplay/
│   ├── rider-design.md
│   ├── shooter-design.md
│   ├── coop-design.md
│   ├── beer-design.md
│   ├── progression-design.md
│   ├── enemy-design.md
│   ├── boss-design.md
│   └── ability-design.md
│
├── 02-run/
│   ├── run-structure.md
│   ├── encounter-design.md
│   ├── event-design.md
│   └── meta-progression-design.md
│
├── 03-world/
│   ├── world-and-level-design.md
│   ├── world-progression.md
│   └── procedural-generation-design.md
│
├── 04-technical/
│   ├── technical-prototype-plan.md
│   ├── technical-architecture.md
│   ├── networking-design.md
│   └── save-system-design.md
│
├── 05-production/
│   ├── playtest-plan.md
│   ├── production-roadmap.md
│   ├── art-direction.md
│   ├── audio-design.md
│   └── ui-ux-design.md
│
└── 06-release/
    ├── qa-test-plan.md
    ├── accessibility-design.md
    └── marketing-and-store-page.md
```

## My actual recommendation for you now

**Stop writing design documents for a while.** You already have enough to start building the next prototype.

I would build in this order:

1. **Make driving feel good**
2. **Add a second player**
3. **Add basic shooting**
4. **Add enemies**
5. **Add ramming**
6. **Add beer and intoxication**
7. **Create one small level**
8. **Playtest it with another person**
9. **Only then write `playtest-plan.md` based on what you actually discovered**

The most important thing you can learn now is not another theoretical design idea. It is whether the sentence:

> **"I am driving a shopping cart while my friend shoots things from it."**

is actually fun when you play it.

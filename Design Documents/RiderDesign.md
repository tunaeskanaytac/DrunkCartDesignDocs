# Rider Design

## Purpose

The Rider is responsible for controlling the shopping cart.

The Rider's role must be more than:

> **Hold forward and steer.**

The Rider should have meaningful decisions involving:

* Positioning
* Momentum
* Risk
* Timing
* Vehicle abilities
* Collision
* Intoxication management

The central design goal is:

> **The Rider should feel like they are piloting an unstable weapon while trying to create opportunities for the Shooter.**

---

# The Rider's Core Fantasy

The Rider is not simply a driver.

The Rider is:

> **A person trying to control an increasingly powerful and increasingly uncontrollable shopping cart while navigating a dangerous battlefield.**

The fantasy should be:

```text
Build Momentum
    ↓
Choose a Maneuver
    ↓
Create an Advantage
    ↓
Take a Risk
    ↓
Recover Control
    ↓
Repeat
```

The Rider should constantly be asking:

> **Can I get away with this?**

---

# Rider Gameplay Loop

```text id="qg83n7"
Observe Battlefield
    ↓
Choose Position
    ↓
Build / Preserve Momentum
    ↓
Choose Maneuver
    ↓
Help Shooter or Attack with Cart
    ↓
Avoid Consequences
    ↓
Recover
    ↓
Repeat
```

The Rider should not simply navigate from one location to another.

Movement should be the primary form of decision-making.

---

# Core Driving Model

The cart should behave like a lightweight vehicle.

It should have:

* Acceleration
* Maximum speed
* Friction
* Turning
* Momentum
* Braking
* Collision response

The Rider should feel the difference between:

```text
High Speed
    ↓
Harder to Turn
    ↓
Greater Collision Potential
    ↓
Greater Risk
```

And:

```text
Low Speed
    ↓
Better Control
    ↓
Less Escape Potential
    ↓
Less Collision Damage
```

This creates a basic risk/reward relationship.

---

# Momentum

Momentum should be the foundation of the Rider's gameplay.

The Rider should not be able to instantly stop and rotate like a character.

Instead:

```text
Current Velocity
        ↓
Steering Input
        ↓
Change in Direction
        ↓
Acceleration / Friction
        ↓
New Velocity
```

The cart should have a physical feeling without becoming frustrating.

---

# Speed and Control

A useful relationship:

```text
Low Speed
├─ Easy to turn
├─ Easy to stop
└─ Low impact damage

High Speed
├─ Harder to turn
├─ Harder to stop
└─ High impact damage
```

This gives the Rider a constant choice:

> **Do I want control or power?**

---

# The Rider's Main Decisions

The Rider should regularly choose between:

## Maintain Speed

Benefits:

* More damage
* Better escape potential
* More momentum

Risks:

* Difficult turning
* Difficult braking
* Greater collision risk

---

## Slow Down

Benefits:

* Better control
* Better positioning
* Easier aiming for the Shooter

Risks:

* More vulnerable
* Easier for enemies to surround the cart

---

## Turn Aggressively

Benefits:

* Can avoid enemies
* Can reposition the Shooter

Risks:

* Loses momentum
* May spin into danger

---

## Ram

Benefits:

* Deals damage
* Clears enemies
* Can create space

Risks:

* Collision damage
* Loss of control
* Potentially getting surrounded

---

# Recommended Initial Ability Set

The Rider should initially have only a few abilities.

## Steering

The basic movement ability.

---

## Brake

Reduces speed quickly.

The Brake should be useful but have a cost.

Possible costs:

* Loses momentum
* Creates vulnerability
* Has a cooldown
* Causes a skid

---

## Drift

Allows the cart to rotate while preserving momentum.

The Drift should be a skill-based tool.

Potential uses:

* Dodge enemies
* Make sharp turns
* Reposition the Shooter
* Maintain speed through corners

---

## Boost

Provides a temporary burst of acceleration.

The Boost should be useful for:

* Escaping
* Chasing rewards
* Ramming enemies
* Crossing dangerous areas

---

# The Rider as a Combatant

The Rider should have an offensive role.

The cart itself should be capable of dealing damage.

Basic collision damage:

```text id="09a0y5"
Collision Damage
=
Speed
×
Impact Strength
×
Cart Upgrades
```

The Rider should be able to intentionally attack enemies.

This gives the Rider a combat loop:

```text id="h5if1d"
Choose Target
    ↓
Build Speed
    ↓
Approach
    ↓
Ram
    ↓
Deal Damage
    ↓
Escape
```

The Rider should not be forced to attack enemies constantly.

Ramming should be a risk/reward decision.

---

# Collision Design

Collisions should not simply mean:

> **Hit enemy → deal damage → continue moving.**

The impact should have consequences.

Possible outcomes:

### Light Impact

* Enemy takes damage
* Cart loses some speed

### Heavy Impact

* Enemy takes significant damage
* Cart loses momentum
* Rider may be displaced

### Dangerous Impact

* Cart hits an obstacle
* Cart loses control
* The team becomes vulnerable

This creates a difference between:

> **A good ram**

and:

> **A desperate crash**

---

# Cart Abilities

The Rider can eventually build around different cart abilities.

## Ram Build

Focus:

* Collision damage
* Knockback
* Armor
* Speed

Gameplay:

> **Become a weapon.**

---

## Drift Build

Focus:

* Turning
* Momentum retention
* Evasion
* Mobility

Gameplay:

> **Avoid everything while maintaining speed.**

---

## Speed Build

Focus:

* Acceleration
* Maximum speed
* Boost

Gameplay:

> **Move so quickly that enemies cannot keep up.**

---

## Defensive Build

Focus:

* Armor
* Damage reduction
* Collision resistance
* Recovery

Gameplay:

> **Survive dangerous situations and protect the Shooter.**

---

## Control Build

Focus:

* Braking
* Turning
* Traction
* Intoxication resistance

Gameplay:

> **Maintain control even when the game becomes chaotic.**

---

# Intoxication and Rider Gameplay

Intoxication should directly affect the Rider's challenge.

The preferred approach is to alter the handling model.

Possible effects:

## Increased Momentum

The cart takes longer to stop.

---

## Reduced Traction

The cart slides during turns.

---

## Increased Acceleration

The cart reaches high speed faster.

---

## Reduced Braking

The cart requires more distance to stop.

---

## Increased Turning Sensitivity

Small steering inputs produce larger changes.

---

The goal is:

> **The Rider must adapt to the current physical condition of the cart.**

The cart should become more difficult, but not randomly uncontrollable.

---

# Intoxication as a Difficulty Curve

Example:

```text
SOBER
    ↓
Normal Handling

TIPSY
    ↓
Slightly More Momentum

DRUNK
    ↓
Reduced Traction

WASTED
    ↓
Extreme Momentum and Speed
```

The Rider should gradually learn:

> **This is how the cart handles at this level of intoxication.**

This allows intoxication to become a skill challenge.

---

# Beer Should Change the Rider's Strategy

The Rider should sometimes want the Shooter to drink.

This is important.

If the Rider always hates beer, then the mechanic creates conflict but not cooperation.

Potential synergies:

### High Intoxication = High Speed

The Rider may use the increased speed offensively.

---

### High Intoxication = Better Shooter

The Shooter can eliminate threats more quickly.

---

### Intoxication-Based Upgrades

The Rider can choose upgrades that make intoxication more manageable.

Example:

> **Drunk Driver**
> The cart gains better handling as intoxication increases.

This creates a build where:

> **The Rider actively wants the Shooter to become drunk.**

---

# The Rider Should Control Positioning

The Shooter should not be able to independently move the cart.

The Rider controls the team's position.

This creates an important cooperative relationship.

The Shooter may say:

> "Move closer."

The Rider may say:

> "We can't."

The Shooter may say:

> "Turn left!"

The Rider may say:

> "I'm trying!"

This communication should emerge naturally from gameplay.

---

# Shooter Positioning

The Rider should affect:

* Shooter line of sight
* Enemy distance
* Shooting angles
* Access to rewards
* Escape routes

The Rider should be able to help the Shooter by:

* Turning toward enemies
* Maintaining firing distance
* Creating clear angles
* Moving toward targets

The Shooter should be able to help the Rider by:

* Clearing escape paths
* Killing enemies approaching from the side
* Removing dangerous targets
* Protecting the cart during maneuvers

---

# The Rider's Battlefield Role

The Rider should control:

```text
Where the team is
        ↓
What enemies are nearby
        ↓
What targets the Shooter can reach
        ↓
What escape routes exist
```

The Shooter controls:

```text
Which enemies die
        ↓
How quickly they die
        ↓
Which rewards become available
```

This creates a useful division of responsibility.

---

# The Rider Should Have Spatial Goals

The Rider should not simply move randomly through an empty arena.

The environment should create movement decisions.

Possible spatial features:

* Narrow paths
* Open arenas
* Obstacles
* Ramps
* Destructible objects
* Dangerous zones
* Reward locations
* Enemy spawning areas

The Rider should think:

> **Where should I be?**

not merely:

> **Which direction should I press?**

---

# Environmental Interaction

The cart can interact with the environment.

Possible interactions:

## Destructible Objects

The cart can crash through them.

---

## Ramps

The cart can jump.

---

## Slopes

The cart gains or loses speed.

---

## Narrow Passages

The Rider must control the cart precisely.

---

## Dangerous Terrain

Examples:

* Mud
* Ice
* Fire
* Water
* Slopes

These can temporarily change handling.

The environment should create situations where the Rider's vehicle skills matter.

---

# Rider Skill Ceiling

The Rider's skill should come from:

## Prediction

Knowing where the cart will be in a few seconds.

---

## Momentum Management

Knowing when to accelerate and brake.

---

## Positioning

Creating good opportunities for the Shooter.

---

## Risk Assessment

Knowing when to ram and when to escape.

---

## Recovery

Regaining control after a bad maneuver.

---

# The Recovery Skill

A particularly important mechanic is recovering from mistakes.

The Rider should not instantly die after making one mistake.

Instead:

```text
Mistake
    ↓
Lose Momentum / Control
    ↓
Become Vulnerable
    ↓
Recover
    ↓
Escape or Counterattack
```

This creates moments of tension.

A good Rider should be able to say:

> **I messed up, but I can still save this.**

---

# The Rider's Core Skill Test

The Rider should be able to answer:

> **Can I turn a bad situation into a good one through skill?**

Examples:

* A bad turn becomes a drift
* A missed ram becomes an escape
* A dangerous enemy group becomes an opportunity
* A loss of control becomes a momentum-based maneuver

This is more interesting than simply avoiding all mistakes.

---

# The Rider's Upgrade Philosophy

Rider upgrades should not only be numerical.

They should change how the cart is played.

Examples:

### Better Numbers

> +10% acceleration

Useful, but not especially transformative.

---

### New Behavior

> The cart can perform a second drift during a single maneuver.

More interesting.

---

### New Strategy

> The cart gains damage based on the distance traveled since the last collision.

This creates an entirely new playstyle.

The best upgrades should change decisions.

---

# Example Rider Upgrades

## Reinforced Basket

The cart takes less collision damage.

---

## Spiked Front

The cart deals additional damage when ramming.

---

## Emergency Brake

Perform a powerful instant brake with a cooldown.

---

## Loose Wheel

Higher maximum speed but reduced turning control.

---

## Turbo Engine

Boost becomes stronger.

---

## Greased Wheels

Higher speed and lower traction.

---

## Heavy Frame

More collision damage and armor, but slower acceleration.

---

## Drunk Driver

The cart gains improved handling at high intoxication.

---

## Momentum Storage

The cart stores some momentum when braking and can release it as a boost.

---

## Dangerous Steering

Turning becomes much more powerful but harder to control.

---

# Rider and Shooter Synergy

The best builds should connect both players.

## Speed + Fire Rate

### Rider

High speed.

### Shooter

Increased attack speed while moving quickly.

---

## Ram + Explosion

### Rider

High collision damage.

### Shooter

Enemies hit by the cart explode when killed.

---

## Drift + Precision

### Rider

Maintains speed while turning.

### Shooter

Gains accuracy while the cart is drifting.

---

## Intoxication + Handling

### Shooter

More powerful while drunk.

### Rider

Better handling at high intoxication.

---

# The Rider's Core Resource

The Rider may eventually benefit from having a resource.

Possible resources:

* Boost charges
* Momentum
* Stamina
* Heat
* Traction

The simplest initial resource is:

> **Boost charges**

This gives the Rider an explicit decision:

```text Use Boost Now
    or
Save Boost for Later
```

Do not add too many resources at once.

---

# Prototype Version of the Rider

The first version should contain only:

```text id="x3x9tq"
Acceleration
    +
Steering
    +
Braking
    +
Momentum
    +
Drift
    +
Boost
    +
Collision Damage
```

This is enough to test the Rider role.

Do not implement every possible mechanic before testing this version.

---

# Recommended Initial Control Model

The cart should feel:

* Heavier than a character
* More responsive than a realistic vehicle
* Less predictable than a normal arcade car
* More controllable than a physics object

The desired feeling is:

> **Arcade vehicle physics with meaningful momentum.**

Avoid:

* Completely realistic vehicle simulation
* Fully physics-driven chaos
* Instant character-like turning

---

# Rider Playtest Questions

After each playtest, ask:

### Driving

* Did the cart feel satisfying to control?
* Did momentum matter?
* Did braking feel meaningful?
* Did turning feel predictable?

### Combat

* Did ramming feel powerful?
* Did the Rider have reasons to attack?
* Was the risk worth the reward?

### Cooperation

* Did the Rider feel important to the Shooter?
* Did the Shooter's position matter?
* Did the Rider have control over the team's situation?

### Intoxication

* Did the changing handling feel interesting?
* Did it feel challenging rather than frustrating?
* Did the Rider learn to adapt?

### Progression

* Did Rider upgrades change gameplay?
* Did different builds feel distinct?

---

# The Rider's Success Criteria

The Rider role is successful if:

```text id="y0a2c8"
The Rider enjoys controlling the cart
        AND
Movement requires decisions
        AND
Momentum creates skill expression
        AND
The cart can be used offensively
        AND
The Shooter depends on Rider positioning
        AND
Intoxication creates an interesting handling challenge
```

---

# Final Design Principle

The Rider should not be:

> **The player who drives the Shooter around.**

The Rider should be:

> **The player who controls the team's position, momentum, escape routes, and physical weapon.**

The Shooter controls:

> **Power.**

The Rider controls:

> **Position.**

Beer creates the conflict:

> **More power makes position harder to control.**

That relationship should remain at the center of the Rider's design.

---

# Core Rider Fantasy

The ideal Rider experience is:

```text
"I have a plan."
    ↓
"I have momentum."
    ↓
"I can make this."
    ↓
"Why are we going so fast?"
    ↓
"TURN!"
    ↓
"TURN!"
    ↓
"TURN!"
    ↓
"WE'RE FINE."
```

The Rider should create the physical chaos.

The Shooter should create the combat chaos.

The game should emerge from both forms of chaos happening at the same time.

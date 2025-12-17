# AI Video Physics Experiment Plan

This plan outlines a structured approach to evaluating how well generative AI models simulate real-world physics. Current models (like Sora, Runway Gen-3, Pika) often prioritize visual realism over physical correctness, leading to "dream-like" physics where objects morph or vanish.

## Core Evaluation Dimensions

We will test 4 key dimensions that are notoriously difficult for AI:

1. **Rigid Body Dynamics & Collisions**: how solid objects interact.
2. **Fluid Dynamics**: Liquids, smoke, and complex flows.
3. **Object Permanence & Consistency**: Things staying the same when moving or hidden.
4. **Causal Reasoning**: Cause and effect relationships (time).

## Test 1: Rigid Body Dynamics (The "Glass Tower" Test)

AI often struggles with the conservation of mass and momentum during destruction.

- **Prompt**: "A tall tower made of clear glass blocks collapsing in slow motion after being hit by a wrecking ball."
- **What to watch for**:
  - **Shattering timing**: Does the glass break *on impact* or randomly?
  - **Piece consistency**: Do the shards look like pieces of the original blocks, or do they disappear/morph into liquid?
  - **Gravity**: Do pieces fall at a consistent speed, or do they float?

## Test 2: Fluid Dynamics (The "Coffee Spill" Test)

Liquids require simulating thousands of particles, which is hard for video diffusion models.

- **Prompt**: "A cup of hot coffee spilling onto a white marble table in slow motion. Steam rises from the liquid."
- **What to watch for**:
  - **Viscosity**: Does the coffee flow like water/liquid, or does it look like sludge or disappear?
  - **Interaction**: Does the liquid spread naturally across the surface or just "paint" the surface?
  - **Steam**: Does the steam move independently of the liquid?

## Test 3: Object Permanence (The "Occlusion" Test)

When an object goes behind another, AI models often forget it exists.

- **Prompt**: "A red sports car driving behind a row of thick stone pillars. It enters from the left and exits on the right."
- **What to watch for**:
  - **Consistency**: Is it the *same* car when it reappears? (Check wheels, color, shape).
  - **Existence**: Does the car flicker or disappear while "behind" the pillar?
  - **Timeline**: Does it travel at a consistent speed behind the pillars?

## Test 4: Causal Reasoning (The "Domino" Test)

Testing if the AI understands that event A must cause event B.

- **Prompt**: "A complex line of dominoes falling. The last domino hits a small switch that turns on a light bulb."
- **What to watch for**:
  - **Sequence**: Do the dominoes fall *because* the previous one hit them, or do they all just start falling randomly?
  - **Trigger**: Does the light turn on *exactly* when the switch is hit, or before/after?

## Test 5: The "Anti-Physics" Control

See if the AI can handle impossible physics vs. real physics.

- **Prompt**: "A heavy stone floating upwards like a balloon in a park."
- **What to watch for**: A good model should be able to visualize this *if prompted*, but it distinguishes it from the default "gravity" behavior in other prompts.

## Scoring Sheet (0-5)

For each model and video, rate:

-  **Visual Realism (0-5)**: Does it look like a photo?
-  **Physical Plausibility (0-5)**: Does it follow laws of physics?
-  **Temporal Consistency (0-5)**: Do objects flicker or morph over time?
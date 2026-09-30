# Lunar Lander

A single-file Lunar Lander game built with **Pygame**. Pilot the lander with vector-based thrust and gravity, manage its fuel, and land safely on one of two procedurally generated pads.

## Features

- Horizontal screen wrapping and a top boundary that keeps the ship visible
- Rotational controls, gravity, directional thrust, and limited fuel
- Two landing pads per terrain, with different score multipliers
- Landing validation for pad alignment, horizontal speed, downward speed, and ship angle
- Crash messages that identify the reason for an unsafe landing
- Score, levels, lives, and an extra life for every 1,500 points earned
- Hull color that shifts toward red as fuel runs low
- Fireworks after successful landings, with a larger display for higher-scoring landings

## Requirements and setup

Use Python 3.10 or newer. Install Pygame and start the game:

```bash
pip install pygame
python game.py
```

## Controls

- **Left / Right:** Rotate the ship
- **Up:** Apply thrust while fuel remains
- **Space:** Start the next level after landing, or retry after a crash while lives remain
- **R:** Restart the game

## Landing and game rules

A landing succeeds only when the ship is fully over a pad, its horizontal speed is at most `MAX_SPEED_X`, its downward speed is between zero and `MAX_SPEED_Y`, and its angle is within `MAX_ANGLE`. Flying upward, drifting too quickly, landing too fast, or missing a pad causes a crash and costs one life.

Fuel is clamped at zero. Thrust switches off when fuel is depleted. The game ends when no lives remain; press **R** to restart.

## Project files

```text
lunar_lander/
|-- game.py
`-- README.md
```

## Lab submission checklist

- [ ] A 10-second gameplay video before the changes, showing the original bug or incomplete behavior
- [ ] A 10-second gameplay video after the changes, showing safe landing validation and the added features
- [ ] A link to the LLM conversation with the complete chat history

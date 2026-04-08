# Asterisk Remastered

Asterisk Remastered is a browser-based remake of the classic 1980s reflex game. This version is built as a single self-contained `index.html` file using HTML5 Canvas and JavaScript, so it runs in any modern browser with no build step or external assets.

## How To Play

Open `index.html` in a browser.

- Hold `Enter` to rise.
- Release `Enter` to fall.
- Reach the glowing gap on the right wall to advance to the next level.
- Avoid the top and bottom walls and every 2x2 obstacle block.
- If you crash, the game shows a game-over screen and you can restart with `Enter`.

## Features

- Single-player Canvas port of the original Asterisk gameplay loop.
- Obstacles rendered as 2x2 white blocks.
- Increasing difficulty each level through added obstacles, faster movement, and a smaller exit gap.
- Countdown before each run and level.
- Score, level display, and persistent high score with `localStorage`.
- Dynamic background colors, glowing trail effects, and simple browser-generated sound effects.

## Project Notes

The game logic lives entirely inside `index.html` so the submission stays self-contained. There is no setup process beyond opening the file in a browser.

## Reflection

We used AI as a rapid prototyping partner to translate the old desktop-style game loop into a browser-friendly Canvas version, then iterated on the generated structure instead of accepting it blindly. AI was especially useful for getting the initial render loop, keyboard handling, and level-generation ideas moving quickly, but we still had to review the output carefully to make sure the port matched the assignment requirements instead of just producing a generic obstacle game. That review step mattered most around the control scheme, because the game needs "hold Enter to rise, release to fall" rather than a tap-to-jump mechanic.

The biggest manual fixes were around gameplay feel and correctness. We adjusted the collision logic so the player only clears a level by reaching the right-side gap, tightened the obstacle placement so random generation would not create unfair spawns near the entry and exit, and tuned the difficulty ramp so the game gets harder in a visible way each round. We also added creative touches beyond the base port, including a countdown, persistent high score, glowing trail, color-shifting background, and lightweight sound cues. In practice, AI helped us move faster, but the final polish came from testing, rewriting pieces of the generated logic, and correcting places where the first draft was technically valid but not yet fun or faithful.

# Part 1: Game Runner

This part sets up the basic game runner for our Pong game. It includes everything needed to start the game loop and render updates at 60 frames per second.

## What's in This Part

- Creates a canvas and sets its size
- Sets up double-buffering (front and back canvases) to avoid flickering
- Maintains a consistent 60 FPS loop
- Separates the `update()` and `draw()` steps for better control
- Adds keyboard event listeners
- Optionally shows FPS and timing stats

## How It Works

We have a `Game.Runner` that handles the main loop. It uses `requestAnimationFrame()` to sync the rendering and ensures we don't exceed the target FPS.

When `initialize()` is called:
- It checks for browser compatibility (like canvas support).
- It creates both the front (visible) and back (off-screen) canvas.
- Sets up a drawing context and starts the game loop.
- Attaches event listeners for keydown/keyup to support player controls.

Stats (like FPS) are shown in the top-left if enabled.

## Running It

Just open the `index.html` in your browser to see the game loop in action. You won’t see the actual game yet — just a black screen being redrawn at 60fps — but it means the runner is working.

```bash
open part1/index.html

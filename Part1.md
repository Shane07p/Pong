# Pong Game - Part 1: Game Runner

This is **Part 1** of a modular Pong game written in pure JavaScript and HTML5 canvas. It sets up a reusable game loop engine and compatibility layer for older browsers.

---

## 🕹 Overview

This part sets up the basic game runner for our Pong game. It includes everything needed to start the game loop and render updates at 60 frames per second.

The `Game` module is a simple engine designed to handle:

- **Cross-browser compatibility**
- **Game loop (update + render)**
- **Double-buffered canvas drawing**
- **Keyboard input**
- **Basic stats display (FPS, frame time, etc.)**

This allows any canvas-based game (like Pong) to focus purely on gameplay logic.

---

## ✅ What's in This Part

- Creates a canvas and sets its size
- Sets up double-buffering (front and back canvases) to avoid flickering
- Maintains a consistent 60 FPS loop using `requestAnimationFrame()`
- Separates the `update()` and `draw()` steps for better control
- Adds keyboard event listeners (`keydown` / `keyup`)
- Optionally shows FPS and timing stats in the top-left corner

---

## ⚙️ How It Works

We use a `Game.Runner` object to handle the main loop.

When `initialize()` is called:

- It checks for browser compatibility (like canvas and audio support).
- Creates both the front (visible) and back (off-screen) canvases.
- Sets up drawing context and starts the game loop.
- Attaches event listeners for keydown/keyup to support player input.
- Optionally displays debug stats (like FPS, frame time, etc.).

The loop is maintained at 60fps using `requestAnimationFrame`, and avoids screen tearing with double buffering.

---

## 🔍 Features

- `Game.Runner`: Manages timing, input, drawing, and stats
- Polyfills for:
  - `Function.prototype.bind`
  - `Object.create`
  - `Object.construct` (custom helper)
  - `Object.extend`
- Canvas and audio support detection
- Basic user-agent parsing for compatibility features

---

## 🚀 Running

To use the runner for your game:

```js
Game.ready(function() {
  var pong = Game.start('game', Pong);
});

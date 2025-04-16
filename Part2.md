# JavaScript Pong - Part 2: Add Ball Bouncing

Welcome to **Part 2** of the JavaScript Pong project!  
In this stage, we introduce **basic ball physics** to bring the game to life — now the ball moves and bounces around the court!

---

## 🎯 What’s New in Part 2

We’ve added the logic that allows the ball to move and bounce off the walls. Here's what we implemented:

- Created a `Ball` object with:
  - Position (`x`, `y`)
  - Velocity (`dx`, `dy`)
  - Radius and color
- The ball moves using delta time (`dt`)
- Bounces off the court walls (top, bottom, left, right)
- Uses random colors and movement directions
- Rendered as a circle using the Canvas API

---

## 🔧 Files Updated
- `index.html`  
  Remains mostly unchanged, except for linking to the updated `pong.js`.

- `pong.js`  
  - Added a `Ball` class.
  - Created a `ball` object and initialized it with random velocity.
  - Updated the `update()` function to move the ball.
  - Handled wall collision (top and bottom).
  - Used `drawCircle()` to render the ball on screen.

##  Ball Physics Explained

- The ball moves using the formula:
  ```js
  ball.x += ball.dx * dt;
  ball.y += ball.dy * dt;  
### ✅ `index.html`

- Mostly unchanged
- Still includes:
  ```html
  <canvas id="game"></canvas>
  <script src="game.js"></script>
  <script src="pong.js"></script>

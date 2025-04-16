# JavaScript Pong - Part 2: Add Ball Bouncing 

Welcome to **Part 2** of the JavaScript Pong project!  
In this stage, we introduce basic ball physics to bring the game to life — now the ball moves and bounces around the play area!

##  What’s New in Part 2

In this part, we:

- Added a **Ball** object with position, velocity, and radius.
- Implemented **movement** based on velocity and time delta.
- Made the ball **bounce off the top and bottom walls**.
- Rendered the ball using `canvas` API.

##  Files Updated

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

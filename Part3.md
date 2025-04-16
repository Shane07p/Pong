# 🏓 JavaScript Pong - Part 3: Add Paddle Physics

Welcome to **Part 3** of the JavaScript Pong series!  
This part adds paddles to the game and introduces basic collision between the ball and the paddles.

## 🔧 What’s in Part 3

- Created a **Paddle** class with position, size, and movement speed.
- Implemented **keyboard controls** for player movement.
- Added **collision detection** between the ball and the paddle.
- Reflected the ball’s velocity when it hits the paddle.
- Limited paddle movement within the canvas bounds.

## 📂 Files Updated

- `index.html`  
  No major changes here — still links to the updated `pong.js`.

- `pong.js`  
  - Added `Paddle` class.
  - Created a `paddle` instance (player-controlled).
  - Handled player input using `keyboard.left` and `keyboard.right`.
  - Added collision check between ball and paddle.
  - Ball bounces off the paddle using velocity inversion.

### 🎮 Paddle Movement

```js
if (keyboard.left) {
  paddle.x -= paddle.speed * dt;
} else if (keyboard.right) {
  paddle.x += paddle.speed * dt;
}

# 🎮 Part 5: Add AI Opponent 🤖

## 🎯 Objective
Introduce a basic AI-controlled paddle that competes against the player, creating a single-player game mode.

## ✨ Features Implemented
- Added AI paddle at the top of the canvas
- Simple tracking behavior based on ball direction
- Collision detection for AI paddle
- Ball now interacts with both player and AI paddles
- Boundary checking for AI movement

## ⚙️ How It Works

### AI Movement Logic
The AI paddle follows these rules:
1. Monitors the ball's horizontal direction (`ball.dx`)
2. Moves left when ball is moving left
3. Moves right when ball is moving right
4. Stays within canvas boundaries

### Collision System
- When ball contacts AI paddle:
  - Bounces downward (toward player)
  - Maintains realistic physics

## 📝 Code Implementation

```javascript
// AI Paddle initialization
const aiPaddle = {
  x: canvas.width / 2,
  y: 30,
  width: 100,
  height: 15,
  speed: 5,
  color: '#FF5555'
};

// AI Movement Update
function updateAI() {
  if (ball.dx < 0 && aiPaddle.x > 0) {
    aiPaddle.x -= aiPaddle.speed; // Move left
  } else if (ball.dx > 0 && aiPaddle.x < canvas.width - aiPaddle.width) {
    aiPaddle.x += aiPaddle.speed; // Move right
  }
}

// Enhanced collision detection
function checkAICollision() {
  if (
    ball.y - ball.radius <= aiPaddle.y + aiPaddle.height &&
    ball.y + ball.radius >= aiPaddle.y &&
    ball.x + ball.radius >= aiPaddle.x &&
    ball.x - ball.radius <= aiPaddle.x + aiPaddle.width
  ) {
    ball.dy = Math.abs(ball.dy); // Reverse vertical direction
    // Optional: Add speed variation based on hit position
    const hitPosition = (ball.x - aiPaddle.x) / aiPaddle.width;
    ball.dx += (hitPosition - 0.5) * 2; // -1 to 1 range
  }
}

##  Part 4: Add AI Opponent

###  Objective
Introduce a basic AI-controlled paddle at the top of the canvas that competes against the player.

###  Features Implemented
- Added a **second paddle** (the AI) at the top of the canvas.
- The AI paddle **tracks the direction** of the ball (`ball.dx`) and moves left or right accordingly.
- Implemented **collision detection** for the ball with the AI paddle.
- Ball now bounces off **both paddles** (player and AI).

###  How It Works
- The AI checks the **horizontal direction** of the ball.
- It moves left or right based on whether the ball is going left or right.
- When the ball touches the AI paddle, it **bounces down**.
- AI paddle stays within the canvas bounds.

###  Outcome
This makes the game **playable** against a simple but functional computer opponent.

---
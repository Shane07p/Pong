##  Part 5: Add Scoring System

###  Objective
Add scoring and create a complete playable game loop where players can win or lose.

###  Features Implemented
- Introduced `playerScore` and `aiScore` to track scores.
- Added a **reset mechanism** to reposition the ball after each point.
- Displayed scores on screen using canvas text rendering.
- Implemented **score detection**:
  - Player scores when ball goes off the **top**.
  - AI scores when ball goes off the **bottom**.

###  How It Works
- Each time the ball crosses the top or bottom edge of the canvas, the appropriate player gets a point.
- The game **resets the ball** to the center after every point.
- The score is displayed at the center of the screen — one for each player.

###  Outcome
The game now has a **competitive goal** — score more than your opponent.
"""
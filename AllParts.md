
---

## 🧩 Part-by-Part Breakdown

### 🔹 Part 1 – Static Game Objects

**Goal**: Set up the canvas and draw the initial game components (ball and court).  
**What’s inside**:
- Basic HTML canvas setup
- Court and ball drawn using simple shapes
- No movement or interaction yet

 *Learning*: HTML5 Canvas basics, drawing shapes, initial layout

---

### 🔹 Part 2 – Bouncing Ball with Game Loop

**Goal**: Animate the ball with velocity and bounce off canvas edges.  
**What’s inside**:
- Time-based `requestAnimationFrame` loop
- Ball updates position using velocity and delta time (`dt`)
- Wall collision detection and response

 *Learning*: Game loops, time step updates, modular game object structure

---

### 🔹 Part 3 – Player Paddle with Keyboard Input

**Goal**: Add a player-controlled paddle using keyboard input.  
**What’s inside**:
- Paddle object with position and velocity
- Arrow key or WASD control
- Paddle stays within the screen

*Learning*: Handling user input, constraining movement, player control

---

### 🔹 Part 4 – Ball & Paddle Collision

**Goal**: Implement paddle-ball collision so the ball bounces back.  
**What’s inside**:
- Paddle and ball collision detection using AABB
- Ball reflects based on point of contact
- Game begins to resemble classic Pong

 *Learning*: Collision detection, vector reflection, gameplay tuning

---

### 🔹 Part 5 – Full Game Logic

**Goal**: Complete the game with scoring, opponent AI, and reset.  
**What’s inside**:
- AI-controlled opponent paddle (follows the ball)
- Score tracking for both players
- Game reset on score with start/stop control

*Learning*: Simple AI logic, state management, finishing touches

---

## 🛠️ How to Run

1. Clone or download this repository.
2. Open any `index.html` inside a part folder using a browser.
3. Explore each part to see the game's evolution!

```bash
git clone https://github.com/Shane07p/Pong.git
cd Pong/part1

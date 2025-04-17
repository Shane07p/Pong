# 🎮 Pong- Part-3

A minimalist 2D Pong game built using vanilla JavaScript and HTML5 Canvas. No external libraries. No AI. Pure 2-player arcade fun!

---

## 🚀 Features

- **Two-Player Gameplay**
- **Scoring System**
- **Victory Condition (First to 10)**
- **Ball Reset After Each Score**
- **Score Display on Screen**
- **ESC Key to Quit to Menu**

---

## 🕹️ Controls

| Action              | Key        |
|---------------------|------------|
| Left Paddle Up      | `Q`        |
| Left Paddle Down    | `A`        |
| Right Paddle Up     | `P`        |
| Right Paddle Down   | `L`        |
| Quit to Menu        | `ESC`      |
| Start 2P Game       | `2`        |

---

## 📦 Project Structure


---

## ⚙️ How It Works

- The `Game.Runner` manages the game loop: `update()` + `draw()` at 60 FPS
- Menu image is shown at startup prompting `1` or `2` (only `2` used)
- Paddle inputs move left/right player
- Ball bounces on paddles and walls
- If the ball exits screen horizontally, opponent scores
- First to reach **10 points** wins
- Pressing `ESC` will quit back to the menu

---

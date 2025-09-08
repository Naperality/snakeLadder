# 🟦 Snake and Ladder – Board Unit

The **Board Unit** represents the physical game board.  
It handles **player positions, snakes, and ladders** as well as game state updates.
---

## 📌 Responsibilities

- Store board layout (snakes and ladders mapping).
- Track each player’s current position.
- Update positions after dice rolls.
- Send feedback to the Control Unit.

---
## 🔧 Hardware Used
- **Microcontroller** (Arduino / ESP32 / Pico)
- **LED Matrix / LCD** – to display board and player tokens.
- **Optional Servos** – to move physical tokens.
- **UART/I2C/SPI** – for communication with Control Unit.
---

## ⚙️ How it Works
1. Receives dice roll result from **Control Unit**.
2. Updates the player’s position on the board.
3. Checks for **snake or ladder rules**:
   - If a player lands at the bottom of a ladder → climb up.
   - If a player lands on a snake head → slide down.
4. Sends updated position back to the Control Unit.

---

## 📜 Example Data Exchange

- Control Unit → Board Unit:  
  `"PLAYER1:ROLL=4"`
- Board Unit → Control Unit:  
  `"PLAYER1:POS=17"`

---

## 🚀 Running the Board Unit

1. Upload the provided Arduino/Pico/ESP32 code to your board.
2. Connect to the Control Unit via **UART/I2C/SPI**.
3. Observe updates on the display as players move.
---

## 📂 Folder Structure

```
BoardUnit/
│── src/ # Source code for Board Unit
│── README.md # Documentation (this file)
```
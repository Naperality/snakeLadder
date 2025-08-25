# 🎮 Snake and Ladder – Control Unit

The **Control Unit** acts as the game controller.  
It manages **dice rolls, user input, and game flow**, while delegating board logic to the Board Unit.

---

## 📌 Responsibilities
- Handle dice roll mechanism (button press / random generator).
- Send dice result to Board Unit.
- Receive updated positions from Board Unit.
- Display current game status (turns, positions, winner).
- Ensure correct turn order for multiple players.

---

## 🔧 Hardware Used
- **Microcontroller** (Arduino / ESP32 / Pico)
- **Push Button / IR Sensor** – for dice roll input.
- **OLED / LCD Display** – to show dice results and player status.
- **UART/I2C/SPI** – communication with Board Unit.

---

## ⚙️ How it Works
1. Player presses the dice button.
2. Control Unit generates a random number (1–6).
3. Sends the roll result to the Board Unit.
4. Receives new player position from the Board Unit.
5. Updates display with game status.
6. Continues until a player reaches the finish.

---

## 📜 Example Data Exchange
- Control Unit → Board Unit:  
  `"PLAYER2:ROLL=6"`
- Board Unit → Control Unit:  
  `"PLAYER2:POS=21"`

---

## 🚀 Running the Control Unit
1. Upload firmware to the microcontroller.
2. Connect push button and display module.
3. Establish communication link with Board Unit.
4. Start the game by pressing the button.

---

## 📂 Folder Structure

```
ControlUnit/
│── src/ # Source code for Control Unit
│── README.md # Documentation (this file)
```

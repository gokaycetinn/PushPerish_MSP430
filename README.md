# 🎮 CENG 329 Project: Push or Perish

A competitive reaction-based game built using the MSP430 microcontroller, a 7-segment display, buttons, and LEDs. Two players compete by strategically timing their button presses according to countdown logic.

---

## 👥 Team Members

- Hasan Emre Usta – 202111301  
- Gökay Çetinakdoğan – 202111050  
- Kayra Dalçık – 202111023  

---

## 🎯 Objective

The objective of this project is to design and implement a competitive game using:

- MSP430 Microcontroller
- 7-segment display
- Two buttons
- Two LEDs

The game, **"Push or Perish,"** requires players to press buttons strategically to win based on predefined rules.

---

## 🛠 Project Specifications

### ⏳ Countdown Mechanism

- 7-segment display counts down from **3 to 0** (1-second interval).
- When countdown reaches **0**, display shows a dash **“-”** to indicate game end.

### 🏁 Win Conditions

- If a player presses **before** countdown ends → **opponent wins**, and their LED lights up.
- If both wait until countdown ends → **first to press** after 0 wins (their LED lights up).

### 🔄 Game Restart

- After a round ends, system **waits 3 seconds** then **automatically restarts**.

---

## 🔧 Components Used

- 1 × MSP430 Microcontroller  
- 1 × 7-Segment Display  
- 2 × Buttons (Player 1 & Player 2)  
- 2 × LEDs (1 per player)

---

## 💻 Implementation Details

### 🔌 Hardware Setup

**LEDs**  
- Player 1 (Red): `P1.0` (Output)  
- Player 2 (Green): `P2.1` (Output)  

**Buttons**  
- Player 1: `P1.3` (Input with pull-up)  
- Player 2: `P2.3` (Input with pull-up)  

**7-Segment Display**  
- Controlled via `P1OUT` and `P2OUT` registers  
- Segments configured using digital I/O  

### 🧠 Software Flow

**Countdown Logic**  
- Each digit (3 to 0) shown using separate subroutines  
- After 0, display shows “-”  

**Button Detection**  
- Constant polling of button states  
- Checks if button was pressed before or after countdown ends  

**LED Control**  
- Premature press → opponent's LED ON  
- Timely press → pressing player’s LED ON  

**Game Reset**  
- 3-second delay  
- Countdown and game logic restart

---

## ✅ Results & Observations

- Game logic works as intended  
- Countdown, button input, and LED output are properly synchronized  
- Players engage in real-time competition  

---

## ⚠️ Challenges

- Precise delay calibration for accurate countdown  
- Debugging hardware wiring for 7-segment display

---

## 📺  Video Demonstration

  
[Watch the Gameplay on YouTube](https://www.youtube.com/shorts/hu23h-f-BZg)



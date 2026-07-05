# 🍬 CANDYTOPIA - A WORLD OF SWEET ADVENTURES 🍬

Welcome to **Candytopia**! This is a whimsical, candy-themed responsive website featuring interactive galleries, a live product showcase, a local-storage backed review system, a custom SVG-to-PNG AI Image Lab simulator, soundscapes built with the Web Audio API, and a custom "Candy Catcher" arcade game.

---
```​
## 📁 PROJECT STRUCTURE

Candytopia Website/

│
├── index.html          # Main web page, styles, and core game logic
├── Readme.md           # Project documentation (this file)
└── Candytopia.png      # Website logo asset (required for header)


---

## 🎮 FEATURE OVERVIEW
1. **Home & Flavor Gallery:** Fully responsive, beautifully animated CSS grids introducing visitors to the sweet kingdoms.
2. **Sweet Treats Shop:** Interactive product catalog with an automated "Add to Cart" notification system.
3. **Sweet Reviews:** Dynamic form allowing users to submit ratings and reviews. Saves instantly to `localStorage` so your custom reviews persist even after a page refresh! Includes a built-in "Delete" and "Clear All" utility.
4. **AI Image Lab:** Canvas-driven playground simulating custom graphic generation with an integrated SVG-to-PNG converter.
5. **Ambient Soundscapes:** Bulletproof Web Audio API synthesizers producing "Bubble Pop", "Chocolate River", and "Soda Fizz" effects dynamically, complete with a standalone offline WAV file exporter.
6. **Candy Catcher Game:** An embedded HTML5 Canvas arcade game featuring an automated difficulty speed scaling system, progressive spawn parameters, hazardous obstacles, and dedicated pause/resume controls.
7. **Sweet Night Mode:** A sticky global theme override switch allowing users to toggle between pastel-light and dark chocolate-dark visuals.

---

## 🕹️ GAMEPLAY CONTROLS & MECHANICS

### Objective
Catch the falling treats using your basket while actively avoiding hazardous items. The game speeds up dynamically as your score climbs to increase the difficulty.

### Controls
* **Basket Movement:** Move your mouse cursor horizontally over the gameplay zone, or use the **LEFT** and **RIGHT** Arrow keys on your keyboard.
* **Pause / Resume:** Press the **ENTER** key at any point during gameplay to freeze the action. Press the **ENTER** key again while paused to instantly resume.
* **Direct Canvas Interaction:** Clicking the custom *"Restart Game"* button drawn directly inside the canvas while the game is paused will safely reset your run.

### Item Behaviors & Logic
* **Normal Sweets (🍬, 🍭, 🐻, 🍫, 🍩):** Must be caught to advance your score.
* **Bombs (💣) & Skulls (💀):** Must be completely dodged! These hazard items drop with a **+0.8 velocity speed bonus** relative to standard sweets to test your split-second reflexes.

### Win / Loss Conditions
* **Game Over (Dropped Sweet):** Triggered instantly if you let a single good candy slip past your basket.
* **Game Over (Hazard Strike):** Triggered instantly if your basket touches a falling Bomb (💣) or Skull (💀).
* **Safe Fall:** Letting a Bomb or Skull drop past the bottom of the screen is completely safe, causing them to wipe cleanly from active memory arrays.
* **Game Win:** Successfully catch your way to a perfect score of **100** to achieve the ultimate sugar rush victory screen!

---

## 🚀 HOW TO RUN THE WEBSITE
1. Ensure you have the `Candytopia.png` logo file located in the exact same directory as your `index.html`.
2. Double-click `index.html` to open it in any modern web browser (Chrome, Firefox, Edge, or Safari).
3. *(Optional)* For the best experience using the Web Audio soundscapes, running the folder via a local server extension (like VS Code's "Live Server") ensures flawless browser security permissions.

---

## 🛠️ CUSTOMIZATION NOTES
* **Input Conflict Prevention:** Migrating the pause/resume mapping from the Spacebar to the **ENTER** key safeguards the application against unexpected window scrolling behavior and prevents accidental whitespace inputs while users type out text reviews.
* **Safe Repaint Loop:** The restart routines are structurally isolated to completely kill prior active `requestAnimationFrame` cycles, preventing accidental speed-layering bugs.
* **Difficulty Tweaking:** To adjust the game difficulty manually, open `index.html` and locate the `update()` function. You can tweak the `adjustedSpawnDelay` variable values to make the candies spawn faster or slower.
* **Grid Customization:** Custom background grid sizes can be modified within the `body` and `body.dark-mode` CSS blocks inside the global `<style>` block.

---
### Thank you for exploring Candytopia! Made with sweet imagination. 🍩

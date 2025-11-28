# Element-Quest
# Engine: Godot 4.5.1

## How to Play
1. Clone or Download this repository.
2. Open Godot Engine (Version 4.5.1).
3. Click "Import" and go inside the `Element Quest` folder and select 'element-quest' folder.
4. Click Select This Folder.
5. Press F5 (Play) to start the game.

# Game Design Overview
1. The Core Objective
The player must traverse from the Sky to Earth to complete three sequential tasks, acquire essential gear, and defeat the Final Boss. Constraint: The entire run must be completed within a global time limit of 5 minutes.

2. Controls
Mouse Left Click: Interact with UI (Select Cards, Use/Sell/Skip buttons).
Spacebar: Attack Boss, Enter Portals, Trigger Teleports, Jump.

3. Game Progression (The Loop)
Phase A: Preparation (Sky Scene)
- Spawn: Player begins in the Sky
- Action: Acquire the Wind Card
- Inventory: Card appears in the Backpack (Options: Use or Sell)
- Transition: Press Spacebar at the portal to travel to the Map -> Select Earth.

Phase B: The Earth Hub (Central Connector) The Hub connects three tasks that must be completed in a strict order.
- Task 1: Always Open.
- Task 2: Locked 🔒 (Requires Key).
- Task 3: Locked 🔒 (Requires Sword).

Phase C: The Tasks
- Task 1: Enter -> Locate and pick up the Key -> Teleport back.
- Task 2: Enter (using Key) -> Locate and pick up the Sword -> Teleport back.
- Task 3: Enter (using Sword) ->  Boss Fight.

4. Core Mechanics
❤️ Health & Combat
- Boss Damage: The boss has a "Damage Zone." Standing inside it drains -10 HP per second.
- Attacking: Press Spacebar near the boss to attack.
- Death: Game Over if HP reaches 0.

🍃 Item System: The Wind Card
- Effect: Restores +20 HP.
- Condition: Can only be used if current HP is < 50 (Button is locked if HP $\ge$ 50).
- Cost: Consumables are removed from the bag upon use.

🃏 Reward System (Post-Boss)
- Trigger: Occurs immediately upon defeating the Boss.
- Visual: Cards shuffle on screen.
- Player Choice:
   1. Pick a Card: Adds item to bag -> Click "Continue."
   2. Skip: Click "Skip Reward" immediately to finish.

5. Win & Loss Conditions
🏆 Victory Conditions The player wins ONLY if:
1. All 3 tasks are completed.
2. The Boss is defeated.
3. Global Timer is under 5 minutes.

💀 Game Over Conditions The player loses if:
1. Time Out: The 5-minute global timer expires.
2. Death: Player HP drops to 0.

# Setup for marketplace
PS C:\Users\Chong Yan Qi\Desktop\elements-quest24112025> npm create vite@latest marketplace --template react
Need to install the following packages:
create-vite@8.2.0
Ok to proceed? (y) y


> npx
> create-vite marketplace react

│
◇  Select a framework:
│  React
│
◇  Select a variant:
│  JavaScript
│
◇  Use rolldown-vite (Experimental)?:
│  No
│
◇  Install with npm and start now?
│  Yes
│
◇  Scaffolding project in C:\Users\Chong Yan Qi\Desktop\elements-quest24112025\marketplace...
│
◇  Installing dependencies with npm...


npm init -y
npm install express cors body-parser
node server.cjs
npm run dev

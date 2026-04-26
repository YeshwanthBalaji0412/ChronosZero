# Chronos Zero
### UE5 Stealth-to-Escape Game | CSYE7270 Final Project

A single-mission stealth game built entirely in Unreal Engine 5 using Visual Blueprints.
Infiltrate an AI-controlled facility, retrieve the Data Core, and escape before the
15-second alarm countdown ends.

---

## Core Concept
The same physical space transforms emotionally and mechanically the moment the alarm
triggers. Cold blue stealth phase. Frantic red escape phase. One transition moment.

**Before alarm** — controlled, slow, strategic
**After alarm** — urgent, reactive, high pressure

---

## Gameplay
- Infiltrate a 6-zone AI facility undetected
- Collect keycards to unlock doors between zones
- Hold-to-interact with the Data Core in Zone 4
- Alarm triggers — lights flood red, 15-second timer starts
- Reach the extraction point in Zone 6 before time runs out

---

## Features
- Patrol drone enemy with dot product vision cone and line trace detection
- Detection modifier system — crouch reduces detection chance by 70%
- Frame-rate independent stamina system with auto-cancel sprint
- Blue to red dynamic lighting transition on alarm trigger
- Keycard and door interaction system across all 6 zones
- Hold-to-interact Data Core pickup
- 15-second escape countdown timer
- Full HUD — stamina bar, timer, interaction prompts
- Win and lose screens with restart button
- Main menu and How to Play screen
- Mixamo character — Jennifer rigged as Astra

---

## Tech Stack
- Engine: Unreal Engine 5 — Third Person Template
- Language: Visual Blueprints — no C++
- UI: UMG Widget Blueprints
- Character: Mixamo — Adobe
- Platform: PC

---

## Level Design
| Zone | Name | Description |
|------|------|-------------|
| 1 | Entry | Player spawn, first keycard location |
| 2 | Patrol Zone | Drone patrol, crate cover, keycard gate |
| 3 | Mid Corridor | Narrow exposed corridor, no cover |
| 4 | Core Vault | Data Core pedestal, two exits, alarm trigger |
| 5 | Escape Route | L-shaped corridor, sprint required |
| 6 | Exit | Extraction point, win trigger |

---

## Blueprints
- **BP_ThirdPersonCharacter** — stamina, crouch, detection modifier, interact input
- **BP_PatrolDrone** — patrol movement, vision cone, line trace, detection timer
- **BP_GameMode_CZ** — alarm state, countdown timer, win/lose logic, lighting transition
- **BP_DataCore** — hold-to-interact, alarm trigger on pickup
- **BP_Door_ZX** — keycard gate, alarm-triggered lock system
- **WBP_HUD** — stamina bar, countdown timer, interaction prompt
- **WBP_GameOver** — lose screen, restart button
- **WBP_Victory** — win screen, restart button
- **WBP_MainMenu** — play, how to play, quit
- **WBP_HowToPlay** — controls reference screen

---

## Controls
| Input | Action |
|-------|--------|
| WASD | Move |
| Left Shift | Sprint (drains stamina) |
| C | Crouch (reduces detection by 70%) |
| E (hold) | Interact |

---

## How to Run
1. Clone the repository
2. Open ChronosZero.uproject in Unreal Engine 5
3. Press Play or package for Windows

---

## Links
- **GitHub:** https://github.com/YeshwanthBalaji0412/ChronosZero.git
- **Gameplay Video:** https://youtu.be/U46wT32sx34?si=7V0TTyG9CaqkSVwA


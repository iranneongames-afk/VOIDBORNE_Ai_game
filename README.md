# VOIDBORNE

**Survive the swarm.**

A neon arena survival shooter that lives in a single HTML file. No build step, no
dependencies, no assets — just open it in a browser. Runs on desktop and mobile.

---

## What it is

You're dropped into a glowing arena and have to hold out against escalating waves
of geometric enemies. Kill fast, chain combos, and bank energy to trigger a
bullet-time Overdrive before the swarm overwhelms you.

Everything — rendering, audio, input, UI — is hand-rolled vanilla JavaScript.

---

## Features

**Gameplay**
- Five enemy archetypes: `Drone`, `Weaver`, `Sniper`, `Orbiter`, and `Brute`
  (Brutes split into smaller drones on death)
- Endless wave system — enemy count, HP, speed, and variety scale every wave
- Combo multiplier up to ×10, with a decay window that punishes passivity
- `Overdrive`: a charged bullet-time mode with faster fire rate, slowed enemies,
  and a full palette shift
- Dash with i-frames and a cooldown ring
- Magnetised pickups: energy orbs for Overdrive, rare health drops
- Best score persisted to `localStorage`

**Presentation**
- Parallax starfield, drifting nebulae, animated neon grid, and vignette
- Glow sprites, particle systems, shockwave rings, dash trails, screen shake,
  hit-stop, and damage flash
- CRT scanlines and subtle film grain for a retro-cyberpunk feel
- Fully procedural sound design via Web Audio — no audio files
- DPR-aware rendering (capped at 2×) with automatic scaling

**Interface**
- Complete HUD: score, best, health pips, wave counter, combo readout,
  Overdrive meter, pause
- Start menu, pause screen, and game-over screen with run stats and a
  "new record" callout

---

## Controls

| Action | Desktop | Mobile |
| --- | --- | --- |
| Move | `W` `A` `S` `D` / arrow keys | Left virtual stick |
| Aim | Mouse | Right virtual stick, or auto-lock |
| Fire | Automatic | Automatic |
| Dash | `Space` | `DASH` button |
| Overdrive | `E` | `OVERDRIVE` button |
| Pause | `Esc` / `P` | Pause icon |
| Mute | `M` | — |

Aim assist locks onto the nearest enemy when no manual aim input is given.

---

## Tech

- Vanilla JavaScript (ES6+), no frameworks or bundlers
- Canvas 2D for all rendering
- Web Audio API for synthesised SFX
- `localStorage` for the high score
- Touch, mouse, and keyboard input in one unified loop
- Single file, zero dependencies, works offline

---

## Running it

Clone the repo and open the file:

```bash
git clone https://github.com/<your-username>/voidborne.git
cd voidborne
open index.html   # or just double-click it

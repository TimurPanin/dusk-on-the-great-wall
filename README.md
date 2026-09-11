# Legend of the Red Dragon

A small browser-based pixel action game prototype built with **Phaser 3, TypeScript and Vite**.

The project focuses on game-loop structure, combat, enemy behaviour, procedural pixel-art generation and a compact retro-style UI rather than external art assets.

## Current status

**Prototype / work in progress.**

The repository currently contains one playable level with a start menu, side-scrolling gameplay, several enemy types, collectibles, a boss encounter, game-over flow and a victory screen.

## Features

- Pixel-art rendering with Phaser Arcade Physics
- Side-scrolling level with camera follow and parallax background
- Player movement with jump buffering and coyote time
- Melee attacks and charged spirit projectile
- HP and lives system with temporary invincibility after damage
- Three regular enemy behaviours:
  - Flying Demon
  - Hellhound
  - Imp
- Boss encounter with a shockwave attack
- Collectibles and score system
- Collapsing platform and spike hazards
- HUD with lives, HP, score, spirit cooldown and combo indicator
- Persistent high score stored in `localStorage`
- Procedurally generated pixel-art textures
- Procedurally generated sound effects through the Web Audio API

## Controls

| Action | Keys |
|---|---|
| Move | `←` / `→` or `A` / `D` |
| Jump | `Z`, `W` or `Space` |
| Melee attack | Tap `X` or `K` |
| Spirit blast | Hold and release `X` or `K` |
| Mute | `M` |
| Start / confirm | `Enter` |

## Tech stack

- **TypeScript**
- **Phaser 3**
- **Vite**
- **Arcade Physics**
- **Canvas** for generated textures
- **Web Audio API** for generated sound effects

## Project structure

```text
src/
├── entities/           # Player, boss, projectile and enemies
├── game/               # Phaser configuration and shared constants
├── levels/             # Level layout and spawn data
├── scenes/             # Boot, menu, gameplay, HUD, game over and victory
├── systems/            # Combat, parallax and visual feedback systems
├── utils/              # Texture generation and sound effects
└── main.ts             # Application entry point
```

## Run locally

Requirements: **Node.js** and **npm**.

```bash
npm install
npm run dev
```

For a production build:

```bash
npm run build
```

Preview the production build locally:

```bash
npm run preview
```

## Notes

Most visual assets are generated at runtime in `TextureGenerator.ts`, while sound effects are synthesized in `SfxManager.ts`. This keeps the prototype self-contained and makes the rendering/audio implementation visible directly in the source code.

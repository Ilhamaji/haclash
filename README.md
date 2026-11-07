<div align="center">

# Haclash

A **2D hack-and-slash platformer** built with Godot 4.7 and GDScript.

[![Status](https://img.shields.io/badge/status-%F0%9F%9A%A7%20prototype-orange?style=flat-square)](#)
[![Godot](https://img.shields.io/badge/Godot-4.7-478CBF?style=flat-square&logo=godot-engine&logoColor=white)](https://godotengine.org)
[![GDScript](https://img.shields.io/badge/GDScript-4-478CBF?style=flat-square&logo=godot-engine&logoColor=white)](https://docs.godotengine.org)

**English** · [Bahasa Indonesia](README.id.md)

</div>

---

> ## 🚧 This project is still a prototype
>
> The gameplay foundation is in place (movement, platforms, attack and roll animations), but there are **no enemies, no damage system, no level design, and no UI**. All numbers are placeholders and untuned. See the [Roadmap](#-roadmap).

---

## About

Haclash is a 2D *hack-and-slash* experiment: the player moves through a platform arena and attacks enemies with combos. It exists as a way to learn **Godot 4**, particularly `CharacterBody2D`, animation state machines, and scene composition from reusable scenes.

## What Already Exists

- **Player controller** (`scripts/player.gd`) — horizontal movement, jumping, and facing-direction detection.
- **Attack and roll animations** — combo animation logic and a dodge roll (still placeholder).
- **Separate scenes** — `player.tscn`, `platform.tscn`, and `game.tscn` for level composition.
- **Godot 4.7 project** — Forward+ renderer.

## Tech Stack

| Layer | Technology |
| --- | --- |
| Engine | Godot 4.7 |
| Language | GDScript |
| Renderer | Forward+ |
| Assets | SVG (vector icons and sprites) |

## Running It

### 1. Install Godot 4.7

Download from [godotengine.org](https://godotengine.org/download).

### 2. Clone

```bash
git clone https://github.com/Ilhamaji/haclash.git
cd haclash
```

### 3. Open in Godot

Click **Import** → select `project.godot` → **Import & Edit**, then press **F5** to run.

## Project Layout

```
project.godot          # project config (Godot 4.7, Forward+)
icon.svg               # project icon
scenes/
  game.tscn            # main level scene
  player.tscn          # player scene
  platform.tscn        # platform prefab
scripts/
  player.gd            # player controller and state machine
assets/                # sprites and visual assets
```

## 🗺️ Roadmap

### High priority
- [ ] **Enemies** — a base enemy class plus 1–2 types (melee and ranged) with patrol/attack AI.
- [ ] **Damage and health** — hitbox/hurtbox, HP bars, invincibility frames, and knockback.
- [ ] **Explicit player state machine** — separate `Idle / Run / Jump / Fall / Attack / Hurt / Dead`.
- [ ] **Camera** — `Camera2D` with smoothing and level bounds.

### Medium priority
- [ ] **Level design** — one complete level with a start → mid → boss progression.
- [ ] **Tilemap** — replace placeholder platforms with `TileMapLayer`.
- [ ] **Checkpoints and respawn** — a save point mid-level.
- [ ] **UI/HUD** — HP bar, score, pause menu, and game over.
- [ ] **SFX and music** — attack, jump, and background music.

### Low priority
- [ ] **Combo system** — chained attacks with timing windows.
- [ ] **Upgrades and skills** — extra abilities between levels.
- [ ] **Save system** — persist progress and high scores.
- [ ] **Build and distribution** — export to Windows/Linux/Web (HTML5).

### Known gaps and bugs
- [ ] **Roll is still a placeholder** (no invincibility frames yet).
- [ ] There are no enemy scenes at all — the game cannot be played through.
- [ ] No audio assets.
- [ ] Movement parameters (speed, gravity, jump force) are untuned.

---

<div align="center">
Built by <a href="https://github.com/Ilhamaji">Ilham Aji</a>
</div>

<div align="center">

# Haclash

**Game platformer hack-and-slash 2D** yang dibangun dengan Godot 4.7 dan GDScript.

[![Status](https://img.shields.io/badge/status-%F0%9F%9A%A7%20prototype-orange?style=flat-square)](#)
[![Godot](https://img.shields.io/badge/Godot-4.7-478CBF?style=flat-square&logo=godot-engine&logoColor=white)](https://godotengine.org)
[![GDScript](https://img.shields.io/badge/GDScript-4-478CBF?style=flat-square&logo=godot-engine&logoColor=white)](https://docs.godotengine.org)

</div>

---

> ## 🚧 Project ini masih prototype
>
> Fondasi gameplay (gerak, platform, animasi serangan & roll) sudah ada, tetapi **belum ada musuh, sistem damage, level design, atau UI**. Angka masih placeholder dan belum di-tuning. Lihat [Roadmap](#-roadmap).

---

## Tentang

Haclash adalah eksperimen game 2D bergenre *hack-and-slash* — pemain bergerak di arena platform dan menyerang musuh dengan combo. Project ini dipakai untuk mempelajari **Godot 4**, terutama node `CharacterBody2D`, state machine animasi, dan resourse-based scene composition.

## Fitur yang Sudah Ada

- **Player controller** (`scripts/player.gd`) — pergerakan horizontal, lompat, dan deteksi arah hadap.
- **Animasi serangan & roll** — logika animasi combo dan *dodge roll* (masih tahap placeholder).
- **Scene terpisah** — `player.tscn`, `platform.tscn`, dan `game.tscn` untuk komposisi level.
- **Konfigurasi Godot 4.7** — renderer Forward+.

## Tech Stack

| Bagian | Teknologi |
| --- | --- |
| Engine | Godot 4.7 |
| Bahasa | GDScript |
| Renderer | Forward+ |
| Aset | SVG (ikon & sprite vektor) |

## Menjalankan

### 1. Install Godot 4.7

Unduh dari [godotengine.org](https://godotengine.org/download).

### 2. Clone repo

```bash
git clone https://github.com/Ilhamaji/haclash.git
cd haclash
```

### 3. Buka di Godot

Klik **Import** → pilih `project.godot` → **Import & Edit**, lalu tekan **F5** untuk run.

## Struktur

```
project.godot          # konfigurasi project (Godot 4.7, Forward+)
icon.svg               # ikon project
scenes/
  game.tscn            # scene level utama
  player.tscn          # scene player
  platform.tscn        # prefab platform
scripts/
  player.gd            # controller & state machine player
assets/                # sprite dan aset visual
```

## 🗺️ Roadmap

### Prioritas Tinggi
- [ ] **Musuh** — base class musuh + 1–2 tipe (melee & ranged) dengan AI patroli/serang.
- [ ] **Sistem damage & health** — hitbox/hurtbox, HP bar, invincibility frames, dan knockback.
- [ ] **State machine player** — pisahkan `Idle / Run / Jump / Fall / Attack / Hurt / Dead` secara eksplisit.
- [ ] **Kamera** — `Camera2D` dengan smoothing dan batas level.

### Prioritas Menengah
- [ ] **Level design** — 1 level utuh dengan progres awal → tengah → boss.
- [ ] **Tilemap** — ganti platform placeholder dengan `TileMapLayer`.
- [ ] **Checkpoint & respawn** — titik simpan di tengah level.
- [ ] **UI/HUD** — HP bar, skor, menu pause, dan game over.
- [ ] **SFX & musik** — efek serangan, lompat, dan musik latar.

### Prioritas Rendah
- [ ] **Combo system** — rantai serangan dengan window timing.
- [ ] **Upgrade/skill** — ability tambahan antar-level.
- [ ] **Save system** — simpan progres dan high score.
- [ ] **Build & distribusi** — ekspor ke Windows/Linux/Web (HTML5).

### Diketahui Kurang / Bug
- [ ] Fitur **roll masih placeholder** (belum ada invincibility frame).
- [ ] Belum ada scene musuh sama sekali — gameplay belum bisa dimainkan penuh.
- [ ] Belum ada aset audio.
- [ ] Parameter gerak (kecepatan, gravitasi, jump force) belum di-tuning.

---

<div align="center">
Dibuat oleh <a href="https://github.com/Ilhamaji">Ilham Aji</a>
</div>

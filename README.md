# Sachi's Pookies

**Sachi's Pookies** is a charming memory-based image reveal game where players match tile pairs to uncover hidden images. Designed with vibrant visuals and rewarding progression, this project serves as a test run for an interactive game design, to be deployed on **GitHub Pages** once the core gameplay mechanics are complete.

## Game Objective

Reveal a hidden image by correctly matching all image pairs on a grid. Each successful match reveals a portion of the photo underneath. Complete all pairs to fully reveal a beautiful version of the image and progress to the next level.

## How It Works

- A grid overlays a hidden photo.
- Each tile in the grid contains one of several matching image icons.
- Players flip two tiles at a time to find a matching pair.
- Matching pairs unlock the corresponding section of the photo underneath.
- Every image icon appears exactly **twice** per level.
- When all pairs are matched, the full hidden image is revealed in **sharper, more vibrant detail**.
- Click “Next” to continue to the next level and a brand new image.

## Gameplay Loop

1. **Start Menu**:
   - Start Game
   - View Gallery
   - Exit

2. **In-Game**:
   - Flip tile pairs to match them.
   - If matched: Reveal part of the image.
   - If mismatched: Try again — but only up to 5 wrong attempts per level.

3. **Level Complete**:
   - View the fully revealed image.
   - Click “Next” to go to the next puzzle.

4. **Game Over**:
   - Failing more than 5 match attempts ends the level.
   - Retry from the beginning or main menu.

## Gallery Feature

- Each completed level unlocks a high-resolution version of the hidden image.
- Players can revisit all unlocked images from the Gallery on the main menu.
- Unlock all 12 images by successfully completing all levels.

## Game Progression

- 12 Levels in total, each with a unique hidden photo.
- Matching difficulty increases as levels progress.
- Visual effects and transitions enhance each level reveal.

## Project Purpose

This game is part of a creative front-end project meant to explore:

- Interactive puzzle design
- Animation and grid layout techniques
- Memory-based mechanics
- Dynamic UI transitions

## Deployment Status
![GitHub Pages](https://github.com/Jimmyu2foru18/SachisPookies/workflows/Deploy/badge.svg)

## Installation & Deployment
```bash
# Clone repository
git clone https://github.com/Jimmyu2foru18/SachisPookies.git
cd SachisPookies

# Install dependencies
npm install

# Build for production
npm run build

# Deploy to GitHub Pages
npm run deploy
```

Game will be automatically deployed to:
https://jimmyu2foru18.github.io/SachisPookies/
"""
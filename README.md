# Sachi's Pookies - Memory Match Game

[![Live Demo](https://img.shields.io/badge/Live_Demo-Available_-brightgreen)](https://jimmyu2foru18.github.io/SachisPookies/)  
[![GitHub Pages](https://img.shields.io/badge/GitHub_Pages-Deployed-blue)](https://github.com/Jimmyu2foru18/SachisPookies/deployments)

---

**Sachi's Pookies** is a captivating memory-based matching game where players flip tiles to reveal hidden images and complete picture puzzles. 
With dynamic visuals, smooth animations, and progressive difficulty, this game offers hours of engaging entertainment.

---

## Game Features

### Gameplay
- **10 Exciting Levels**: Progressive difficulty with unique image sets  
- **Memory Challenge**: Classic tile-matching mechanics with modern twists  
- **Timer System**: Track your speed and improve performance  
- **Move Counter**: Challenge yourself to complete levels efficiently  
- **Progressive Unlocking**: Unlock new levels as you progress  

### Design
- **Modern UI/UX**: Clean, intuitive interface with smooth animations  
- **Responsive Design**: Optimized for desktop, tablet, and mobile  
- **Gradient Backgrounds**: Eye-catching visual design  
- **Smooth Animations**: CSS3 transitions and transforms  
- **Emoji Integration**: Fun, engaging visual elements  

### User Experience
- **Main Menu**: Central hub for game options  
- **Level Selection**: Choose from unlocked levels  
- **Instructions Popup**: Comprehensive game tutorial  
- **Pause Functionality**: Take breaks without losing progress  
- **Victory Screen**: Celebrate your achievements  
- **Replay System**: Replay any level to improve your score  

### Progress & Storage
- **Local Storage**: Automatic progress saving  
- **Level Unlocking**: Complete levels to unlock new challenges  
- **Persistent State**: Game remembers your unlocked levels  

---

## How to Play

### Objective
Match all pairs of images by flipping tiles to reveal hidden pictures and complete each level.

### Game Mechanics
1. **Start the Game**: Click "Play Game" from the main menu  
2. **Choose a Level**: Select from available unlocked levels  
3. **Flip Tiles**: Click on tiles to reveal hidden images  
4. **Find Matches**: Select two tiles to find matching pairs  
5. **Complete the Level**: Match all pairs to reveal the victory image  
6. **Progress Further**: Unlock new levels and challenges  

### Tips for Success
- **Memory Training**: Remember the location of revealed images  
- **Strategic Approach**: Start with corners and edges  
- **Take Your Time**: Think before you click  
- **Practice Regularly**: Improve your memory with repeated play  

---

## Technical Implementation

### Architecture
- **HTML / CSS / JavaScript**  
- **Responsive Layout** using Flexbox & Grid  
- **Styling Features**: CSS3 gradients, fonts, box shadows, smooth 60fps animations  
- **JavaScript Features**: ES6+ syntax, event handling, local storage API, timer management  

### Responsive Design
- **Desktop**: Full 4x4 grid layout, large tiles, side-by-side stats, full button layouts  
- **Tablet**: Optimized grid spacing, adjusted font sizes, stacked stats, touch-friendly buttons  
- **Mobile**: Compact grid, vertical button arrangement, simplified stats, large touch targets  

---

## Game Screens

1. **Main Menu**: Play Game, Instructions, Gallery, Quit  
2. **Level Selection**: Visual 3x3 grid, progress indicators, locked levels with padlock icons  
3. **Game Screen**: Timer, move counter, current level, control buttons, 4x4 tile grid  
4. **Victory Screen**: Congratulations message, victory image, performance stats, navigation options  
5. **Pause Modal**: Pause notification, resume, restart level, main menu  

---

## Technical Documentation

### File Structure

~~~bash
SachisPookies/
├── index.html
├── package.json
├── vite.config.js
├── TechnicalDocumentation.md
├── README.md
├── Images/
│   ├── 1.png - 10.png
│   ├── sachi1.png - sachi10.png
│   └── Main Screen Background.png
└── .github/workflows/
    └── deploy.yml
~~~

### Key Functions

- **Game Management**: `showScreen(screenId)`, `startGame(level)`, `createGameGrid()`, `flipTile(tile)`, `checkMatch()`  
- **Timer System**: `startTimer()`, `stopTimer()`, `updateTimer()`  
- **Progress Management**: `updateLevelGrid()`, `showVictory()`, `nextLevel()`  
- **Data Storage**: `localStorage` key `unlockedLevels` (default: Level 1 unlocked, 10 levels total)  

---

## Installation & Setup

### Quick Start
```bash
git clone https://github.com/Jimmyu2foru18/SachisPookies.git
cd SachisPookies
open index.html
```

### Development Setup
```bash
npm install
npm run dev
npm run build
npm run deploy
```

---

## Customization

### Adding New Levels
- Add images to the `Images/` folder  
- Update `maxLevel` in JavaScript  
- Follow the image naming convention  

### Changing Colors
Modify CSS custom properties:
```css
/* Main gradient colors */
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);

/* Button colors */
background: linear-gradient(45deg, #4a90e2, #357abd);
```

### Adjusting Difficulty
- Change `totalPairs` for different grid sizes  
- Modify timer logic for time-based challenges  
- Update level unlocking requirements  

---

## Troubleshooting

- **Images Not Loading**: Check filenames, paths, extensions, and folder placement  
- **Game Not Saving Progress**: Ensure JavaScript is enabled and local storage is allowed  
- **Mobile Display Issues**: Verify viewport meta tag, responsive breakpoints, and touch handling  

---

## Credits

@Th3viousGameus 
@SachiMizora

# 🎮 Sachi's Pookies - Memory Match Game

**Sachi's Pookies** is an enchanting memory-based matching game where players flip tiles to reveal hidden images and complete beautiful picture puzzles. With vibrant visuals, smooth animations, and progressive difficulty, this game provides hours of engaging entertainment for players of all ages.

## 🌟 Features

### ✨ Enhanced Gameplay
- **10 Exciting Levels** - Progressive difficulty with unique image sets
- **Memory Challenge** - Classic tile-matching mechanics with modern twists
- **Timer System** - Track your speed and improve your performance
- **Move Counter** - Challenge yourself to complete levels efficiently
- **Progressive Unlocking** - Unlock new levels as you progress

### 🎨 Beautiful Design
- **Modern UI/UX** - Clean, intuitive interface with smooth animations
- **Responsive Design** - Works perfectly on desktop, tablet, and mobile
- **Gradient Backgrounds** - Eye-catching visual design
- **Smooth Animations** - CSS3 transitions and transforms
- **Emoji Integration** - Fun, engaging visual elements

### 🎯 User Experience
- **Main Menu** - Central hub with all game options
- **Level Selection** - Choose from unlocked levels
- **Instructions Popup** - Comprehensive game tutorial
- **Pause Functionality** - Take breaks without losing progress
- **Victory Screen** - Celebrate your achievements
- **Replay System** - Replay any level to improve your score

### 💾 Progress & Storage
- **Local Storage** - Your progress is saved automatically
- **Level Unlocking** - Complete levels to unlock new challenges
- **Persistent State** - Game remembers your unlocked levels

## 🚀 How to Play

### 🎯 Objective
Match all pairs of images by flipping tiles to reveal the hidden pictures and complete each level.

### 🎮 Game Mechanics
1. **Start the Game** - Click "Play Game" from the main menu
2. **Choose a Level** - Select from available unlocked levels
3. **Flip Tiles** - Click on tiles to reveal hidden images
4. **Find Matches** - Click two tiles to find matching pairs
5. **Complete the Level** - Match all pairs to reveal the victory image
6. **Progress Further** - Unlock new levels and challenges

### 💡 Tips for Success
- **Memory Training** - Try to remember where you've seen images
- **Strategic Approach** - Start with corners and edges
- **Take Your Time** - There's no rush, think before you click
- **Practice Regularly** - The more you play, the better you get

## 🛠️ Technical Implementation

### 🏗️ Architecture
- **Pure HTML/CSS/JavaScript** - No external dependencies
- **Modular Design** - Clean, maintainable code structure
- **Responsive Layout** - Mobile-first design approach
- **Performance Optimized** - Efficient DOM manipulation

### 🎨 Styling Features
- **CSS3 Gradients** - Beautiful background effects
- **Flexbox & Grid** - Modern layout techniques
- **Smooth Animations** - 60fps performance
- **Custom Fonts** - Comic Sans for playful feel
- **Box Shadows** - Depth and visual hierarchy

### ⚡ JavaScript Features
- **ES6+ Syntax** - Modern JavaScript features
- **Event Handling** - Efficient user interaction
- **Local Storage API** - Client-side data persistence
- **Timer Management** - Accurate time tracking
- **Error Handling** - Graceful fallbacks for missing images

## 📱 Responsive Design

### Desktop (1200px+)
- Full 4x4 grid layout
- Large, easy-to-click tiles
- Side-by-side game stats
- Full button layouts

### Tablet (768px - 1199px)
- Optimized grid spacing
- Adjusted font sizes
- Stacked game stats
- Touch-friendly buttons

### Mobile (320px - 767px)
- Compact grid layout
- Large touch targets
- Vertical button arrangement
- Simplified game stats

## 🎯 Game Screens

### 1. Main Menu
- **Play Game** - Start your adventure
- **Instructions** - Learn how to play
- **Gallery** - View completed levels (coming soon)
- **Quit** - Exit the game

### 2. Level Selection
- **Visual Level Grid** - 3x3 grid of available levels
- **Progress Indicators** - Checkmarks for completed levels
- **Lock System** - Locked levels show padlock icons
- **Level Numbers** - Clear level identification

### 3. Game Screen
- **Timer Display** - Real-time elapsed time
- **Move Counter** - Track your efficiency
- **Current Level** - Know which level you're playing
- **Control Buttons** - Pause, Restart, Menu options
- **4x4 Tile Grid** - Main gameplay area

### 4. Victory Screen
- **Congratulations Message** - Celebrate your success
- **Victory Image** - Beautiful completion image
- **Performance Stats** - Time and moves taken
- **Navigation Options** - Next level, replay, menu, level select

### 5. Pause Modal
- **Pause Notification** - Game is paused
- **Resume Option** - Continue playing
- **Restart Level** - Start the level over
- **Main Menu** - Return to main menu

## 🔧 Technical Documentation

### File Structure
```
SachisPookies/
├── index.html              # Main game file
├── package.json            # Project configuration
├── vite.config.js          # Build configuration
├── TechnicalDocumentation.md # UML diagrams & technical specs
├── README.md               # This file
├── Images/                 # Game assets
│   ├── 1.png - 10.png     # Tile images
│   ├── sachi1.png - sachi10.png # Victory images
│   └── Main Screen Background.png
└── .github/workflows/      # CI/CD configuration
    └── deploy.yml
```

### Key Functions

#### Game Management
- `showScreen(screenId)` - Screen navigation
- `startGame(level)` - Initialize new game
- `createGameGrid()` - Generate game board
- `flipTile(tile)` - Handle tile interactions
- `checkMatch()` - Validate tile pairs

#### Timer System
- `startTimer()` - Begin timing
- `stopTimer()` - Pause timing
- `updateTimer()` - Update display

#### Progress Management
- `updateLevelGrid()` - Refresh level selection
- `showVictory()` - Handle level completion
- `nextLevel()` - Progress to next level

### Data Storage
- **Local Storage Keys**:
  - `unlockedLevels` - Number of unlocked levels
- **Default Values**:
  - Start with Level 1 unlocked
  - 10 total levels available

## 🚀 Installation & Setup

### Prerequisites
- Modern web browser (Chrome, Firefox, Safari, Edge)
- Local web server (optional, for development)

### Quick Start
1. **Clone the repository**
   ```bash
   git clone https://github.com/Jimmyu2foru18/SachisPookies.git
   cd SachisPookies
   ```

2. **Open in browser**
   ```bash
   # Simply open index.html in your browser
   open index.html
   ```

### Development Setup
1. **Install dependencies**
   ```bash
   npm install
   ```

2. **Start development server**
   ```bash
   npm run dev
   ```

3. **Build for production**
   ```bash
   npm run build
   ```

4. **Deploy to GitHub Pages**
   ```bash
   npm run deploy
   ```

## 🎨 Customization

### Adding New Levels
1. Add new images to the `Images/` folder
2. Update the `maxLevel` variable in the JavaScript
3. Ensure proper image naming convention

### Changing Colors
Modify the CSS custom properties in the `<style>` section:
```css
/* Main gradient colors */
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);

/* Button colors */
background: linear-gradient(45deg, #4a90e2, #357abd);
```

### Adjusting Difficulty
- Change `totalPairs` variable for different grid sizes
- Modify timer logic for time-based challenges
- Adjust level unlocking requirements

## 🐛 Troubleshooting

### Common Issues

#### Images Not Loading
- Check image file names and paths
- Ensure images are in the correct `Images/` folder
- Verify file extensions (.png)

#### Game Not Saving Progress
- Check browser local storage permissions
- Ensure JavaScript is enabled
- Try refreshing the page

#### Mobile Display Issues
- Check viewport meta tag
- Test responsive breakpoints
- Verify touch event handling

### Browser Compatibility
- **Chrome**: Full support
- **Firefox**: Full support
- **Safari**: Full support
- **Edge**: Full support
- **Mobile browsers**: Full support with responsive design

## 🤝 Contributing

### Development Guidelines
1. Follow existing code style and structure
2. Test on multiple devices and browsers
3. Maintain responsive design principles
4. Keep performance optimizations in mind

### Feature Requests
- New game modes
- Additional animations
- Sound effects integration
- Multiplayer functionality
- Achievement system

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 🙏 Acknowledgments

- **Design Inspiration** - Modern mobile game aesthetics
- **Game Mechanics** - Classic memory matching games
- **Technical Stack** - Pure HTML/CSS/JavaScript approach
- **Community** - Open source contributors and testers

## 📞 Support

For questions, issues, or suggestions:
- **GitHub Issues** - [Create an issue](https://github.com/Jimmyu2foru18/SachisPookies/issues)
- **Documentation** - Check `TechnicalDocumentation.md` for technical details
- **Live Demo** - [Play the game](https://jimmyu2foru18.github.io/SachisPookies/)

---

**Made with ❤️ by the Sachi's Pookies development team**

*Last updated: December 2025*
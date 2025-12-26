# Sachi's Pookies - Technical Documentation

## UML Class Diagram

```mermaid
classDiagram
    class Game {
        -currentLevel: number
        -flippedTiles: array
        -matchedPairs: number
        -totalPairs: number
        -moves: number
        -gameTimer: timer
        -startTime: timestamp
        -isGamePaused: boolean
        -unlockedLevels: number
        -maxLevel: number
        +showScreen(screenId): void
        +showMainMenu(): void
        +showLevelSelect(): void
        +startGame(level): void
        +createGameGrid(): void
        +flipTile(tile): void
        +checkMatch(): void
        +startTimer(): void
        +stopTimer(): void
        +updateTimer(): void
        +pauseGame(): void
        +resumeGame(): void
        +restartLevel(): void
        +showVictory(): void
        +nextLevel(): void
    }

    class Tile {
        -value: number
        -isFlipped: boolean
        -isMatched: boolean
        +flip(): void
        +match(): void
        +reset(): void
    }

    class Screen {
        -screenId: string
        -isActive: boolean
        +show(): void
        +hide(): void
        +toggle(): void
    }

    class Modal {
        -modalId: string
        -isActive: boolean
        +show(): void
        +hide(): void
        +toggle(): void
    }

    class LevelManager {
        -unlockedLevels: number
        -maxLevel: number
        +unlockLevel(level): void
        +isLevelUnlocked(level): boolean
        +getProgress(): object
        +saveProgress(): void
        +loadProgress(): void
    }

    class Timer {
        -startTime: timestamp
        -elapsedTime: number
        -isRunning: boolean
        +start(): void
        +stop(): void
        +pause(): void
        +resume(): void
        +getTime(): string
        +reset(): void
    }

    Game --> Tile : manages
    Game --> Screen : controls
    Game --> Modal : uses
    Game --> LevelManager : uses
    Game --> Timer : uses
    LevelManager --> Timer : tracks
```

## Activity Diagram - Game Flow

```mermaid
flowchart TD
    A[Start Game] --> B[Show Main Menu]
    B --> C{User Action}
    C -->|Play Game| D[Show Level Select]
    C -->|Instructions| E[Show Instructions Modal]
    C -->|Gallery| F[Show Gallery]
    C -->|Quit| G[Exit Game]
    
    D --> H{Level Selected}
    H -->|Valid Level| I[Initialize Game]
    H -->|Back| B
    
    I --> J[Create Game Grid]
    J --> K[Start Timer]
    K --> L[Game Loop]
    
    L --> M{Tile Clicked}
    M -->|First Tile| N[Flip Tile]
    M -->|Second Tile| O[Flip Tile]
    
    N --> L
    O --> P{Check Match}
    
    P -->|Match| Q[Mark as Matched]
    P -->|No Match| R[Flip Back]
    
    Q --> S{All Pairs Matched?}
    S -->|No| L
    S -->|Yes| T[Show Victory Screen]
    
    R --> L
    
    T --> U{User Choice}
    U -->|Next Level| V[Increment Level]
    U -->|Replay| I
    U -->|Level Select| D
    U -->|Main Menu| B
    
    V --> I
    
    L --> W{Game Paused?}
    W -->|Yes| X[Show Pause Modal]
    W -->|No| L
    
    X --> Y{Resume Action}
    Y -->|Resume| L
    Y -->|Restart| I
    Y -->|Main Menu| B
```

## Use Case Diagram

```mermaid
graph LR
    subgraph "Player"
        P1[Start Game]
        P2[Select Level]
        P3[Play Memory Game]
        P4[View Instructions]
        P5[View Gallery]
        P6[Pause Game]
        P7[Restart Level]
        P8[Quit Game]
    end
    
    subgraph "Game System"
        S1[Display Main Menu]
        S2[Show Level Selection]
        S3[Initialize Game Board]
        S4[Handle Tile Clicks]
        S5[Check for Matches]
        S6[Track Game Progress]
        S7[Show Victory Screen]
        S8[Show Game Over Screen]
        S9[Manage Game State]
        S10[Save Progress]
    end
    
    P1 --> S1
    P2 --> S2
    P3 --> S3
    P3 --> S4
    P3 --> S5
    P4 --> S9
    P5 --> S9
    P6 --> S9
    P7 --> S3
    P8 --> S10
    
    S4 --> S5
    S5 --> S6
    S6 --> S7
    S6 --> S8
    S7 --> S10
    S8 --> S10
```

## Design Diagram - System Architecture

```mermaid
graph TB
    subgraph "Frontend Layer"
        UI[User Interface]
        CSS[Styling]
        JS[JavaScript Logic]
    end
    
    subgraph "Game Components"
        GM[Game Manager]
        TM[Tile Manager]
        SM[Screen Manager]
        MM[Modal Manager]
        LM[Level Manager]
        TIMER[Timer System]
    end
    
    subgraph "Data Layer"
        LS[Local Storage]
        IMG[Image Assets]
        STATE[Game State]
    end
    
    subgraph "User Actions"
        CLICK[Click Events]
        NAV[Navigation]
        INPUT[User Input]
    end
    
    UI --> CSS
    UI --> JS
    JS --> GM
    
    GM --> TM
    GM --> SM
    GM --> MM
    GM --> LM
    GM --> TIMER
    
    TM --> CLICK
    SM --> NAV
    MM --> INPUT
    LM --> LS
    TIMER --> STATE
    
    CLICK --> TM
    NAV --> SM
    INPUT --> MM
    LS --> LM
    IMG --> TM
    STATE --> GM
```

## System Components Description

### 1. Game Manager (Core Controller)
- **Purpose**: Central game logic coordinator
- **Responsibilities**: 
  - Game state management
  - Screen transitions
  - Level progression
  - Victory/Game Over conditions

### 2. Tile Manager
- **Purpose**: Manages individual game tiles
- **Responsibilities**:
  - Tile flip animations
  - Match detection
  - Tile state tracking
  - Image loading and display

### 3. Screen Manager
- **Purpose**: Handles different game screens
- **Responsibilities**:
  - Main menu display
  - Level selection
  - Game board rendering
  - Victory/Game Over screens

### 4. Modal Manager
- **Purpose**: Controls popup modals
- **Responsibilities**:
  - Instructions display
  - Pause menu
  - Confirmation dialogs
  - Settings panels

### 5. Level Manager
- **Purpose**: Manages game progression
- **Responsibilities**:
  - Level unlocking
  - Progress tracking
  - Local storage management
  - Difficulty scaling

### 6. Timer System
- **Purpose**: Game timing and scoring
- **Responsibilities**:
  - Elapsed time tracking
  - Move counting
  - Performance metrics
  - High score management

## Data Flow

1. **Game Initialization**: Level Manager → Screen Manager → Game Manager
2. **Tile Interaction**: User → Tile Manager → Game Manager → Screen Manager
3. **Progress Saving**: Game Manager → Level Manager → Local Storage
4. **Screen Transitions**: User → Screen Manager → UI Updates
5. **Modal Interactions**: User → Modal Manager → Game Manager

## Security Considerations

- Local storage data is validated before use
- Image paths are sanitized
- User input is handled through controlled UI elements
- No external API calls or data transmission

## Performance Optimizations

- Efficient DOM manipulation with minimal reflows
- Image preloading for smooth gameplay
- Optimized animations using CSS transforms
- Responsive design for various screen sizes
- Lazy loading of game assets
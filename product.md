# Club Fair Surprise Wheel

## Product Overview

The Club Fair Surprise Wheel is an interactive web-based gamification tool designed to engage students at club fairs and recruitment events. It transforms the traditional club fair experience into an exciting, points-based game where participants spin a virtual wheel to discover clubs and earn scores.

## Purpose

This application serves multiple objectives:
- **Engagement**: Creates excitement and draws participants to the club fair booth
- **Discovery**: Exposes students to various clubs in a fun, memorable way
- **Interaction**: Encourages meaningful engagement with club offerings
- **Competition**: Motivates participation through leaderboard rankings
- **Data Collection**: Captures participant information and club preferences

## Key Features

### 1. Club Configuration System
- **Custom Club Setup**: Administrators can add, remove, and customize clubs
- **Visual Customization**: Each club has a unique color for easy identification
- **Point Assignment**: Automatic point value assignment (50, 75, 100, 125, 150 points)
- **Persistent Storage**: Club configurations are saved locally for future sessions

### 2. Player Registration
- **Name & Class Input**: Collects participant name and class/year information
- **Passport Selection**: Players select 5 clubs as their "passport stamps"
- **Strategic Choice**: Passport selections provide opportunities for bonus multipliers

### 3. Spinning Wheel Mechanics
- **Visual Wheel**: Animated canvas-based wheel with club segments
- **Physics-Based Spin**: Realistic spinning animation with deceleration
- **Audio Feedback**: Dynamic sound effects that vary with wheel speed
- **Pointer Indicator**: Clear visual indicator for winning selection

### 4. Scoring System

#### Base Points
Each club has assigned point values:
- 50 points
- 75 points
- 100 points
- 125 points
- 150 points

#### Multiplier Mechanics

**Passport Match Bonus (2x)**
- If the wheel lands on a club in the player's passport selection
- Doubles the base points for that spin
- Encourages strategic club selection

**Chance Multiplier (Final Spin Only)**
- Applied only on the 3rd and final spin
- Random multiplier: 1.0x, 1.5x, 2.0x, 2.5x, or 3.0x
- Creates dramatic finale and maximum excitement

#### Score Calculation Example
```
Base Points: 100
× 2 (Passport Match)
× 2.5 (Chance Multiplier - Spin 3)
= 500 Final Points
```

### 5. Three-Spin System
- **Spin 1**: Base points with optional passport bonus
- **Spin 2**: Base points with optional passport bonus
- **Spin 3**: Base points + passport bonus + chance multiplier
- Builds anticipation as players progress through their turns

### 6. Leaderboard System
- **Top 15 Display**: Shows top performers
- **Medal System**: 🥇 🥈 🥉 for top 3 positions
- **Current Player Highlight**: Recent player's entry is visually highlighted
- **Persistent Scores**: All scores saved to local storage
- **Class/Year Display**: Shows participant's class information

### 7. Data Management
- **Export Functionality**: Export all scores and club data as JSON
- **Import Functionality**: Import previously exported data
- **Reset Protection**: CAPTCHA-protected score reset to prevent accidental deletion
- **Local Storage**: All data persists in browser local storage

### 8. User Interface Features
- **Responsive Design**: Works on desktop and mobile devices
- **Animated Effects**: Confetti celebrations, glowing text, pulsing buttons
- **Clear Navigation**: Intuitive flow between setup, registration, game, and leaderboard
- **Real-time Updates**: Score displays update immediately during gameplay

## How It Works

### Setup Phase (Administrator)

1. **Initial Configuration**
   - Navigate to the setup screen
   - Add clubs by clicking "Add Club" button
   - Enter club name and select identifying color
   - System automatically assigns point values
   - Click "Launch The Wheel" to start

2. **Default Configuration**
   - Pre-loaded with 13 default clubs:
     - Investment Club, Tech & Innovation Club, Consulting Club
     - Women in Leadership Club, Net Impact Club, Extra Sports Club
     - Culture Club, TedX, Choir, Marketing Club
     - Vali Venture Club, Pride Impact Club, DFS

### Player Experience

1. **Registration**
   - Enter name and class/year
   - View all available clubs in a grid
   - Select exactly 5 clubs as "passport stamps"
   - Click "START SPINNING!" to begin

2. **Gameplay - Spin 1 & 2**
   - Click "SPIN!" button (or press spacebar)
   - Wheel spins with realistic physics and audio
   - Result displays in center screen with:
     - Points earned
     - Calculation breakdown
     - Passport match indicator (if applicable)
   - Click "Next Spin" to continue

3. **Gameplay - Final Spin (Spin 3)**
   - Random chance multiplier announced before spin
   - Displayed as: "🔥 FINAL SPIN! CHANCE MULTIPLIER: 2.5x 🔥"
   - Spin executes with all multipliers
   - Final score calculated and displayed
   - 5-second countdown to leaderboard

4. **Leaderboard**
   - View ranking among all participants
   - Current player highlighted in gold
   - Options to:
     - Register next player
     - Export data
     - Import previous data

### Administrative Controls

Accessible via game screen icons:
- **🏆 Leaderboard**: View current rankings
- **👤 New Player**: Register another participant
- **⚙️ Settings**: Return to club configuration
- **🗑️ Reset Scores**: Clear all scores (with CAPTCHA protection)

## Technical Implementation

### Architecture
- **Single-Page Application**: Pure HTML/CSS/JavaScript
- **No Server Required**: Runs entirely in browser
- **Local Storage**: Data persists using browser localStorage API
- **Canvas API**: Wheel rendering and animation
- **Web Audio API**: Dynamic sound generation

### Key Components

1. **Wheel Engine** (`index.html:650-734`)
   - Canvas-based rendering
   - Rotation physics with friction simulation
   - Real-time redrawing during animation
   - Winning segment calculation

2. **Audio System** (`index.html:858-903`)
   - Dynamic arpeggio sounds varying with wheel speed
   - Win celebration sounds
   - Click feedback effects
   - Web Audio API synthesis

3. **State Management** (`index.html:558-561`)
   - Centralized application state
   - Player data management
   - Spin tracking
   - Multiplier handling

4. **UI Screens** (`index.html:436-519`)
   - Setup Screen: Club configuration
   - Player Screen: Registration and passport selection
   - Game Screen: Wheel and gameplay
   - Leaderboard Screen: Rankings and data management

## Use Cases

### Primary Use Case: Club Fair Event
1. Set up tablet/computer at club fair booth
2. Configure participating clubs
3. Invite students to play
4. Students register and select interests (passports)
5. Students spin and compete for high scores
6. Leaderboard creates ongoing engagement
7. Export data at end of event for analysis

### Secondary Use Cases
- **Orientation Events**: Introduce new students to campus clubs
- **Virtual Fairs**: Remote engagement tool for online events
- **Competitions**: Create tournaments with prizes for top scorers
- **Analytics**: Passport selections reveal club interest patterns

## Benefits

### For Organizers
- Increased booth traffic and engagement
- Memorable participant experience
- Data collection on club interests
- Low setup and technical requirements
- Reusable for multiple events

### For Participants
- Fun, game-like experience
- Exposure to various clubs
- Competitive element with leaderboard
- Visual and audio engagement
- Strategic gameplay through passport selection

### For Clubs
- Increased visibility
- Equal representation on the wheel
- Interest tracking through passport data
- Association with exciting experience

## System Requirements

### Minimal Requirements
- Modern web browser (Chrome, Firefox, Safari, Edge)
- JavaScript enabled
- Local storage enabled
- Display capable of 300px × 300px minimum

### Recommended Setup
- Tablet or laptop with touchscreen
- Screen size: 10 inches or larger
- Recent browser version
- Stable local environment (no internet required)

## Data Privacy

- **Local-Only Storage**: All data stored in browser localStorage
- **No Server Communication**: No data transmitted externally
- **No Tracking**: No analytics or third-party scripts
- **User Control**: Complete control over data export/import/reset
- **Ephemeral Option**: Can be run in incognito mode for no persistence

## Customization Options

### Visual Customization
- Club colors fully customizable
- Point values automatically distributed
- Responsive design adapts to screen size

### Gameplay Customization
Located in `CONFIG` object (`index.html:546-556`):
- `PASSPORT_SLOTS`: Number of clubs players select (default: 5)
- `MATCH_BOOST`: Passport match multiplier (default: 2)
- `CHANCE_MULTIPLIERS`: Available final spin multipliers (default: [1.0, 1.5, 2.0, 2.5, 3.0])

### Club Customization
- Any number of clubs supported (minimum 2)
- Custom names and colors
- Point values auto-assigned but can be modified in code

## Future Enhancement Possibilities

- Multiple point distribution schemes
- Custom wheel themes/skins
- Photo capture for leaderboard entries
- Social media sharing integration
- Multi-event tracking
- QR code check-ins
- Prize tier announcements
- Team/group competitions
- Historical analytics dashboard
- Cloud backup options

## Installation & Deployment

### Local Use
1. Download `index.html` file
2. Open in web browser
3. No installation required

### Web Hosting
1. Upload `index.html` to any web server
2. Access via URL
3. No backend or database required

### Offline Events
1. Load page once while online
2. Works completely offline thereafter
3. All functionality preserved

## Support & Maintenance

The application is self-contained and requires no ongoing maintenance. Data persists in browser storage and can be backed up using the built-in export functionality.

### Backup Procedure
1. Click "Export" button on leaderboard
2. Save JSON file to secure location
3. Import using "Import" button to restore

### Reset Procedure
1. Click reset (🗑️) button
2. Solve simple math CAPTCHA
3. Confirm deletion

## Conclusion

The Club Fair Surprise Wheel combines gamification, visual appeal, and strategic gameplay to create an engaging club fair experience. Its simple setup, browser-based architecture, and competitive elements make it an effective tool for driving participation and creating memorable interactions at student events.

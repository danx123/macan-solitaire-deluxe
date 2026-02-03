# Macan Solitaire Deluxe - Luxury Edition

<div align="center">

**A Premium, Futuristic Klondike Solitaire Game**

*Enterprise-class gaming experience with glassmorphism UI and neon accents*

![Version](https://img.shields.io/badge/version-3.0.0-00d9ff)
![Python](https://img.shields.io/badge/python-3.8+-00d9ff)
![License](https://img.shields.io/badge/license-Proprietary-00d9ff)

</div>

---

## 🌟 Overview

Macan Solitaire Deluxe is not your ordinary solitaire game. Built with premium aesthetics in mind, this luxury edition features a cutting-edge futuristic interface with glassmorphism effects, smooth animations, and elegant neon accents in the signature Macan Angkasa style.

### Design Philosophy

- **Premium First**: Designed to look and feel like an enterprise-class application
- **Minimalist Elegance**: Clean, modern interface without unnecessary clutter
- **Futuristic Aesthetic**: Glassmorphism, blur effects, and cyan neon accents
- **Smooth Experience**: Buttery-smooth animations and responsive interactions

---

## ✨ Features

### 🎨 Visual Excellence
- **Glassmorphism UI**: Translucent, blurred glass-like surfaces
- **Neon Accents**: Electric cyan/blue highlights throughout
- **Custom Window**: Frameless design with rounded corners and drop shadows
- **Premium Cards**: Modern, flat card design with elegant styling
- **Smooth Animations**: Fluid card movements and transitions

### 🎮 Gameplay
- **Classic Klondike**: Traditional solitaire rules you know and love
- **Drag & Drop**: Intuitive card movement
- **Auto-Detection**: Valid moves are highlighted with neon glow
- **Undo System**: Take back your moves
- **Quick Restart**: Start a new game instantly

### 💾 Persistence
- **Auto-Save**: Game state automatically saved
- **JSON Format**: Clean, readable save files
- **Resume Play**: Pick up right where you left off

### 📊 Statistics
- **Real-Time Timer**: Track your game duration
- **Move Counter**: Monitor your efficiency
- **Score Tracking**: Classic solitaire scoring system

---

## 🚀 Installation

### Prerequisites

- Python 3.8 or higher
- PySide6

### Setup

1. **Clone or download** the project files

2. **Install dependencies**:
```bash
pip install PySide6
```

3. **Run the game**:
```bash
python main.py
```

---

## 🎯 How to Play

### Game Rules (Klondike Solitaire)

1. **Objective**: Move all cards to the four foundation piles (top right), sorted by suit from Ace to King

2. **Tableau Rules**:
   - Build down in alternating colors (red on black, black on red)
   - Only Kings can be placed in empty columns
   - You can move sequences of cards together

3. **Foundation Rules**:
   - Must start with Ace
   - Build up by suit (A, 2, 3... K)

4. **Stock/Waste**:
   - Click stock to draw cards
   - Move cards from waste to tableau or foundations

### Controls

- **Left Click**: Select and move cards
- **Drag & Drop**: Move cards between piles
- **New Game**: Start a fresh game
- **Undo**: Reverse your last move
- **✕**: Close the application

---

## 💾 Save System

### Save Location

Game data is automatically saved to:

**Windows**:
```
%LOCALAPPDATA%\MacanSolitaireDeluxe\save.json
```

**Linux/Mac**:
```
~/.local/share/MacanSolitaireDeluxe/save.json
```

### Save Data

The save file contains:
- Current game state (all pile positions)
- Statistics (time, moves, score)
- Game history for undo functionality

Directories are automatically created if they don't exist.

---

## 📦 Building Executable

### Create Standalone EXE (Windows)

1. **Install PyInstaller**:
```bash
pip install pyinstaller
```

2. **Build the executable**:
```bash
pyinstaller --onefile --windowed --name "MacanSolitaireDeluxe" --icon=assets/icon.ico main.py
```

3. **Find your EXE**:
The executable will be in the `dist` folder.

### Build Options

**Single File** (easier distribution):
```bash
pyinstaller --onefile --windowed main.py
```

**Folder Mode** (faster startup):
```bash
pyinstaller --windowed main.py
```

---

## 🗂️ Project Structure

```
macan-solitaire-deluxe/
│
├── main.py                 # Main application file
├── README.md              # This file
│
└── assets/                # Assets folder (optional)
    └── icon.ico          # Application icon
```

---

## 🎨 Design Specifications

### Color Palette

- **Primary Background**: Dark blue-black gradient `rgba(10, 15, 30, 240)`
- **Accent Color**: Cyan neon `#00d9ff`
- **Glass Surfaces**: Semi-transparent with blur
- **Text**: Light blue-white `#e0e7ff`
- **Danger Actions**: Red-pink gradient

### Typography

- **Font Family**: Segoe UI
- **Title**: 18pt Bold
- **UI Elements**: 13-16pt
- **Card Text**: 16-36pt Bold

### Effects

- **Glassmorphism**: Translucent backgrounds with blur
- **Drop Shadows**: Soft cyan glow on interactive elements
- **Hover States**: Brightness increase with glow intensification
- **Animations**: Smooth easing curves for all transitions

---

## 🛠️ Technical Details

### Architecture

- **Single-File Design**: All code in one organized file for simplicity
- **PySide6 Framework**: Modern Qt6 bindings for Python
- **Custom Widgets**: Hand-coded UI components
- **MVC Pattern**: Separation of game logic and presentation

### Performance

- **Efficient Rendering**: Hardware-accelerated graphics
- **Minimal Memory**: Optimized data structures
- **Smooth 60 FPS**: Consistent animation performance
- **Fast Startup**: Lightweight codebase

---

## 🎮 Future Enhancements

Potential features for future versions:

- [ ] Advanced statistics dashboard
- [ ] Multiple theme options
- [ ] Leaderboard system
- [ ] Daily challenges
- [ ] Sound effects and music
- [ ] Customizable card backs
- [ ] Achievement system
- [ ] Multiplayer mode

---

## 📸 Screenshot
<img width="1365" height="767" alt="image" src="https://github.com/user-attachments/assets/f7250538-4546-4571-8438-e1655eb1ac8f" />


## 📝 Development Notes

### Customization

You can easily customize the game by modifying:

- **Colors**: Update the stylesheet in `apply_styles()`
- **Card Design**: Modify `CardWidget.paintEvent()`
- **Window Size**: Change `setFixedSize()` in `__init__`
- **Animation Speed**: Adjust QPropertyAnimation durations

### Adding Features

The modular design makes it easy to extend:

```python
# Example: Add a new button
btn_custom = self.create_button("Custom", self.custom_action)
layout.addWidget(btn_custom)

def custom_action(self):
    # Your custom functionality
    pass
```

---

## 🐛 Troubleshooting

### Common Issues

**Issue**: Window doesn't appear
- **Solution**: Ensure PySide6 is installed: `pip install --upgrade PySide6`

**Issue**: Slow performance
- **Solution**: Update graphics drivers, close other GPU-intensive applications

**Issue**: Save file not found
- **Solution**: Check permissions for the save directory, run as administrator if needed

---

## 📜 License

**© 2026 Macan Angkasa. All rights reserved.**

This is proprietary software developed by Macan Angkasa. Unauthorized copying, modification, distribution, or use of this software is strictly prohibited.



---

## 👨‍💻 Credits

**Developed by**: Macan Angkasa Development Team

**Design**: Macan Angkasa Design Studio

**Special Thanks**: To all solitaire enthusiasts who inspired this luxury edition

---



<div align="center">

**Enjoy the ultimate solitaire experience!**

Made with ❤️ and ☕ by Macan Angkasa

</div>

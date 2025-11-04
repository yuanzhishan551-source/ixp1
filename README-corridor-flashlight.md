# 🔦 The Corridor Flashlight

An immersive first-person horror web experience inspired by pixel horror games. Navigate a dark, eerie corridor using a flashlight with three unique modes to detect and interact with text-based monsters.

![Pixel Horror](https://img.shields.io/badge/Genre-Horror-red)
![Tech](https://img.shields.io/badge/Tech-HTML%20%7C%20CSS%20%7C%20JavaScript-blue)
![Mobile](https://img.shields.io/badge/Platform-Desktop%20%2B%20Mobile-green)

## 🎮 Features

### Three Flashlight Modes

**1. 🟡 Long Beam Mode (Yellow)**
- Narrow, elongated beam with maximum reach
- Reveals red "BUG" monsters at a distance
- Monsters appear with pixel dissolve effect
- Best for scanning distant areas

**2. 🟠 Wide Beam Mode (Orange)**
- Wide, bright light for close-range illumination
- **Freezes** all nearby monsters for 2 seconds
- Emits static click sound on activation
- Best for crowd control

**3. 🟢 Detection Mode (Green)**
- Reveals invisible monsters blending with the environment
- **Disintegrates** green monsters into pixel particles
- Highlights hidden threats
- Best for finding camouflaged entities

### Horror Atmosphere

- **CRT Scanline Effect**: Authentic retro monitor simulation
- **Pixel Noise Overlay**: Dynamic visual grain and static
- **Camera Shake**: Triggers when monsters spawn
- **Parallax Corridor**: Multi-layer depth illusion
- **Flickering Beam**: Random tension-building flickers
- **Procedural Audio**: Ambient drone, glitch bursts, and detection sounds

### Monster System

- **Text-Based Entities**: Glitch typography monsters
- **Multilingual Fragments**: Random error messages in multiple languages
- **Two Monster Types**:
  - **Red Monsters**: Visible in Long Beam mode
  - **Green Monsters**: Nearly invisible, revealed in Detection mode
- **Dynamic Behavior**: Drift, pulse, freeze, and disintegrate
- **Smart Spawning**: Maximum 15 entities for performance
- **Particle Effects**: Green pixel particles on disintegration

## 🎯 How to Play

1. **Open** `corridor-flashlight.html` in any modern web browser
2. **Click** anywhere to start the experience
3. **Move Mouse** to aim the flashlight
4. **Left Click** to cycle through flashlight modes
5. **Survive** and discover all monster types

### Controls

| Action | Desktop | Mobile |
|--------|---------|--------|
| Aim Flashlight | Mouse Movement | Touch & Drag |
| Switch Mode | Left Click | Tap Screen |

## 🛠️ Technical Implementation

### Core Technologies
- **Pure HTML5** - Semantic structure
- **CSS3 Animations** - Parallax, particle effects, glitch animations
- **Vanilla JavaScript** - No frameworks or libraries
- **Web Audio API** - Procedural sound generation

### Key Features

#### Collision Detection
```javascript
// Real-time beam-to-monster collision detection
// Calculates distance between flashlight center and monster position
// Triggers mode-specific reactions
```

#### Mode-Specific Reactions
- **Long Beam**: Pixel dissolve reveal animation
- **Wide Beam**: Animation freeze with timeout
- **Detection**: Disintegration with particle system

#### Performance Optimization
- Monster pool limit (max 15 concurrent)
- Efficient collision checking (50ms intervals)
- CSS transform-based animations (GPU accelerated)
- Automatic cleanup of off-screen entities

#### Responsive Design
- Desktop: Mouse tracking
- Mobile: Touch event support
- Adaptive beam sizes for smaller screens
- Optimized UI for mobile viewports

## 🎨 Visual Style

### Color Palette
- **Background**: Deep blacks (#000, #0a0a0a, #1a1a1a)
- **Long Beam**: Warm yellows (#ffff00, #ff6600)
- **Wide Beam**: Bright oranges (#ff8800, #ff5500)
- **Detection Beam**: Neon greens (#00ff00, #00cc00)
- **Red Monsters**: Crimson (#ff0000)
- **Green Monsters**: Toxic green (#00ff00)

### Typography
- **Font**: VT323 (monospace pixel font)
- **Effects**: Text shadows, glow, glitch distortion
- **Size**: Responsive scaling (16px-32px)

### Effects Stack
1. Parallax corridor layers (3 depths)
2. Pixel noise overlay
3. CRT scanline filter
4. Radial gradient flashlight beam
5. Monster text fragments
6. Particle system
7. Camera shake
8. Glitch text animations

## 📱 Browser Compatibility

Tested and optimized for:
- ✅ Chrome/Edge (latest)
- ✅ Firefox (latest)
- ✅ Safari (latest)
- ✅ Mobile browsers (iOS Safari, Chrome Mobile)

**Requirements**:
- Modern browser with ES6 support
- Web Audio API support (optional, graceful fallback)

## 🔧 Customization

### Adjust Monster Spawn Rate
```javascript
// In the config object (line ~445)
config.spawnRate = 2000; // milliseconds between spawns
```

### Change Maximum Monsters
```javascript
config.maxMonsters = 15; // max concurrent monsters
```

### Modify Beam Flicker Frequency
```javascript
config.beamFlickerInterval = 5000; // flicker every 5 seconds
```

### Add Custom Monster Text
```javascript
// In monsterTexts array (line ~426)
const monsterTexts = [
    'YOUR_TEXT_HERE',
    // ... existing texts
];
```

## 🎵 Audio System

The experience uses the **Web Audio API** for procedural sound generation:

- **Ambient Drone**: 60Hz sine wave oscillator
- **Glitch Bursts**: Random frequency square waves
- **Static Click**: White noise buffer (wide beam mode)
- **Detection Noise**: Sawtooth frequency sweep

All audio is generated in real-time without external files.

## 🏗️ Project Structure

```
corridor-flashlight.html
├── HTML Structure
│   ├── Loading screen
│   ├── Corridor layers (parallax)
│   ├── Monsters container
│   ├── Flashlight beam
│   └── UI overlay
├── CSS Styling
│   ├── Animations (drift, pulse, shake, etc.)
│   ├── Visual effects (scanlines, noise, particles)
│   └── Responsive media queries
└── JavaScript Logic
    ├── Audio system (Web Audio API)
    ├── Flashlight mechanics
    ├── Monster spawning & AI
    ├── Collision detection
    └── Event handling
```

## 🎬 Development Notes

### Design Philosophy
- **Minimalist Horror**: Less is more - tension through atmosphere
- **Retro Aesthetic**: CRT monitors, pixel art, VHS noise
- **Interactive Storytelling**: Environmental narrative through glitch text
- **Performance First**: Smooth 60fps on all devices

### Coding Standards
- **Well-commented**: Every major section explained
- **Modular functions**: Single responsibility principle
- **No dependencies**: Pure vanilla JavaScript
- **Accessibility**: Keyboard/touch support

## 🚀 Future Enhancements

Potential additions:
- [ ] Multiple corridor environments
- [ ] Monster AI pathfinding
- [ ] Score/survival timer
- [ ] More flashlight modes
- [ ] Procedural corridor generation
- [ ] Persistent high scores (localStorage)
- [ ] VR headset support

## 📄 License

Open source - feel free to modify and use in your projects.

## 🙏 Credits

**Created by**: AI Web Designer
**Inspired by**: Pixel horror games, analog horror, glitch art
**Fonts**: Google Fonts (VT323)
**Audio**: Web Audio API (procedural)

---

**Enjoy exploring the darkness... if you dare.** 🔦👾


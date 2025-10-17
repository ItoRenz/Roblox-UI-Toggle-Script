# 🎮 Roblox UI Toggle Button

![Roblox](https://img.shields.io/badge/Roblox-Script-00a2ff?style=for-the-badge&logo=roblox&logoColor=white)
![Lua](https://img.shields.io/badge/Lua-5.1-2C2D72?style=for-the-badge&logo=lua&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)
![Version](https://img.shields.io/badge/Version-3.0-blue?style=for-the-badge)

A modern, ultra-compact, and highly customizable UI toggle button for Roblox games. Hide/show all UI elements with a single click while keeping the toggle button always accessible and non-intrusive.

## ✨ Features

- 🎨 **Modern Design** - Gradient background, glowing effects, and smooth animations
- 📱 **Cross-Platform** - Automatically detects and adapts for PC and Mobile devices
- 🖱️ **Draggable** - Move the button anywhere on your screen with ease
- 💫 **Smooth Animations** - Pulse, breathing, hover, and scale effects
- 🎯 **Smart State Management** - Remembers which UIs were hidden/shown
- 🔄 **Persistent** - Doesn't reset when character respawns
- ⚡ **Lightweight** - Ultra-compact size with optimized performance
- 🎨 **Fully Customizable** - Easy to modify colors, sizes, and behavior
- 🏆 **Competition Ready** - Minimal screen footprint for competitive gameplay

## 📏 Button Sizes

### Current Version (v3.0) - Ultra-Compact
- **PC (Desktop)**: 35 × 22 pixels
- **Mobile (Touch)**: 45 × 28 pixels

### Size History
| Version | PC Size  | Mobile Size | Description      |
|---------|----------|-------------|------------------|
| v1.0    | 40×40px  | 55×55px     | Initial square   |
| v2.0    | 50×30px  | 60×35px     | Rectangular      |
| v3.0    | 35×22px  | 45×28px     | **Ultra-compact** ✨ |

## 🚀 Quick Start

### Method 1: LocalScript (Recommended)
1. Open Roblox Studio
2. Navigate to `StarterPlayer` → `StarterPlayerScripts`
3. Create a new **LocalScript**
4. Copy and paste the code from `ui-toggle.lua`
5. Test in game!

### Method 2: Script Executor
1. Copy the entire script
2. Use your preferred Roblox script executor
3. Execute the script while in-game

## 🎮 How to Use

### Controls
| Action | PC | Mobile |
|--------|----|----|
| **Toggle UI** | Left Click | Tap |
| **Move Button** | Click & Drag | Touch & Drag |
| **Hover Effect** | Mouse Over | N/A |

### Visual Indicators
- 🔵 **Blue Border & Text** - All UIs are visible
- 🔴 **Red Border & Text** - All UIs are hidden
- 💫 **Breathing Animation** - Button is idle and ready
- ✨ **Pulse Effect** - Action confirmed

## ⚙️ Configuration

Customize the button by editing the `SETTINGS` table:

```lua
local SETTINGS = {
    BUTTON_SIZE_PC = UDim2.new(0, 35, 0, 22),      -- PC dimensions
    BUTTON_SIZE_MOBILE = UDim2.new(0, 45, 0, 28),  -- Mobile dimensions
    BUTTON_POSITION = UDim2.new(0, 10, 0, 10),     -- Starting position
    ANIMATION_SPEED = 0.3,                          -- Toggle animation speed
    TEXT_VISIBLE = "UI",                            -- Text when visible
    TEXT_HIDDEN = "UI",                             -- Text when hidden
    COLOR_VISIBLE = Color3.fromRGB(100, 200, 255), -- Blue theme
    COLOR_HIDDEN = Color3.fromRGB(255, 100, 100),  -- Red theme
    ENABLE_DRAGGING = true,                         -- Allow repositioning
    SAVE_POSITION = true                            -- Save position (planned)
}
```

## 🎨 Customization Examples

### 1. Change Button Size
```lua
-- Larger button
BUTTON_SIZE_PC = UDim2.new(0, 50, 0, 30)
BUTTON_SIZE_MOBILE = UDim2.new(0, 65, 0, 40)

-- Smaller button (minimal)
BUTTON_SIZE_PC = UDim2.new(0, 28, 0, 18)
BUTTON_SIZE_MOBILE = UDim2.new(0, 38, 0, 24)
```

### 2. Change Color Theme
```lua
-- Green theme
COLOR_VISIBLE = Color3.fromRGB(0, 255, 127)   -- Emerald green
COLOR_HIDDEN = Color3.fromRGB(255, 69, 0)     -- Orange red

-- Purple theme
COLOR_VISIBLE = Color3.fromRGB(138, 43, 226)  -- Blue violet
COLOR_HIDDEN = Color3.fromRGB(255, 20, 147)   -- Deep pink

-- Dark theme
COLOR_VISIBLE = Color3.fromRGB(200, 200, 200) -- Light gray
COLOR_HIDDEN = Color3.fromRGB(80, 80, 80)     -- Dark gray
```

### 3. Change Button Text
```lua
-- Simple ON/OFF
TEXT_VISIBLE = "ON"
TEXT_HIDDEN = "OFF"

-- Show/Hide
TEXT_VISIBLE = "SHOW"
TEXT_HIDDEN = "HIDE"

-- Custom emoji
TEXT_VISIBLE = "👁️"
TEXT_HIDDEN = "🚫"
```

### 4. Change Position
```lua
-- Top right corner
BUTTON_POSITION = UDim2.new(1, -50, 0, 10)

-- Bottom left corner
BUTTON_POSITION = UDim2.new(0, 10, 1, -40)

-- Center screen
BUTTON_POSITION = UDim2.new(0.5, -20, 0.5, -15)
```

### 5. Disable Dragging
```lua
ENABLE_DRAGGING = false  -- Button stays in fixed position
```

## 🎭 Animation Features

### Included Animations
1. **Pulse Effect** - Glowing animation when button is clicked
2. **Breathing Animation** - Border continuously pulses (2-second cycle)
3. **Hover Effect** - Button scales up 10% on mouse hover (PC only)
4. **Toggle Scale** - Button shrinks 10% when UIs are hidden
5. **Color Transition** - Smooth color change between visible/hidden states

### Animation Settings
```lua
-- Change animation speed
ANIMATION_SPEED = 0.5  -- Slower (default: 0.3)
ANIMATION_SPEED = 0.15 -- Faster
```

## 🛡️ Safety & Performance

### Built-in Safety Features
✅ **Automatic Cleanup** - All tweens and connections properly disposed  
✅ **Error Handling** - Gracefully handles deleted UI elements  
✅ **State Preservation** - Remembers original UI states  
✅ **Memory Management** - No memory leaks  
✅ **Performance Optimized** - Minimal CPU/GPU usage  
✅ **Non-Intrusive** - Doesn't interfere with game mechanics  

### What Gets Hidden?
- All `ScreenGui` objects in `PlayerGui`
- **Except**: The toggle button itself (always visible)
- **Note**: Some protected game UIs may not be affected

## 📋 Technical Details

### Services Used
```lua
Players           -- Player management
UserInputService  -- Input detection & platform ID
TweenService      -- Smooth animations
RunService        -- Frame updates (optional)
```

### UI Hierarchy
```
PlayerGui
└── UIToggleGui (ScreenGui)
    └── ToggleButton (Frame)
        ├── UICorner (Rounded corners)
        ├── UIGradient (Modern gradient)
        ├── UIStroke (Border)
        ├── ShadowStroke (Shadow effect)
        ├── TextButton (Clickable area)
        └── Glow (Frame - Pulse effect)
```

### Platform Detection Logic
```lua
-- Automatic detection
local isMobile = UserInputService.TouchEnabled 
                 and not UserInputService.KeyboardEnabled

-- Result:
-- PC     → Smaller button, hover effects enabled
-- Mobile → Larger button, touch optimized
```

## 🐛 Troubleshooting

### Button not appearing?
**Solution:**
- Ensure script is a **LocalScript** (not a regular Script)
- Place in `StarterPlayer` → `StarterPlayerScripts`
- Check Output console for errors

### Button not hiding specific UIs?
**Solution:**
- Some UIs are protected by the game
- Only affects `ScreenGui` objects in `PlayerGui`
- CoreGui elements cannot be toggled

### Button position resets on respawn?
**Solution:**
- The script uses `ResetOnSpawn = false`
- Position should persist across respawns
- Manual position saving feature is planned for future updates

### Dragging doesn't work on mobile?
**Solution:**
- Touch dragging is supported
- Try a longer press before dragging
- Make sure `ENABLE_DRAGGING = true` in settings

### Animations look choppy?
**Solution:**
- Check your device performance
- Reduce animation speed: `ANIMATION_SPEED = 0.5`
- Close other resource-intensive programs

### Button too small/large?
**Solution:**
- Adjust `BUTTON_SIZE_PC` or `BUTTON_SIZE_MOBILE` in settings
- Recommended minimum: 25×18px (PC), 35×24px (Mobile)
- Recommended maximum: 80×50px (PC), 100×60px (Mobile)

## 🔄 Changelog

### [3.0.0] - Current Version
**Changed:**
- Significantly reduced button size for ultra-compact design
  - PC: 35×22px (was 50×30px) - 30% smaller
  - Mobile: 45×28px (was 60×35px) - 25% smaller
- Optimized text size for better readability at small scale
  - PC: 11px (was 14px)
  - Mobile: 13px (was 16px)

**Improved:**
- Minimal screen footprint for competitive gameplay
- Non-intrusive professional appearance
- Perfect balance between visibility and compactness

**Maintained:**
- All animations and visual effects
- Dragging functionality
- Cross-platform support
- Touch-friendly interaction zones

### [2.0.0] - Previous Version
**Changed:**
- Icon changed from symbols (☰/✕) to "UI" text
- Rectangular button shape (was square)
- Button dimensions adjusted for text display

**Added:**
- GothamBold font for modern appearance
- Improved text rendering

### [1.0.0] - Initial Release
**Added:**
- Basic toggle functionality
- Modern UI design with gradients
- Cross-platform support
- Draggable button
- Smooth animations
- State management

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

### Ways to Contribute
- 🐛 Report bugs via Issues
- 💡 Suggest new features
- 🔧 Submit pull requests
- 📚 Improve documentation
- ⭐ Star the repository

### Pull Request Guidelines
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License.

```
MIT License

Copyright (c) 2025

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

## 🌟 Support

If you find this project useful:
- ⭐ Star this repository
- 🔀 Fork it for your own projects
- 📢 Share it with others
- 💬 Leave feedback in Issues

## 📊 Stats

![GitHub stars](https://img.shields.io/github/stars/username/roblox-ui-toggle?style=social)
![GitHub forks](https://img.shields.io/github/forks/username/roblox-ui-toggle?style=social)
![GitHub issues](https://img.shields.io/github/issues/username/roblox-ui-toggle)

## 📧 Contact & Support

- **Issues**: [GitHub Issues](https://github.com/username/roblox-ui-toggle/issues)
- **Discussions**: [GitHub Discussions](https://github.com/username/roblox-ui-toggle/discussions)
- **Questions**: Open an issue with the "question" label

## 🎯 Roadmap

### Planned Features
- [ ] Position saving between sessions
- [ ] Multiple theme presets
- [ ] Keybind support for toggling
- [ ] Animation customization GUI
- [ ] Per-UI toggle controls
- [ ] Sound effects option
- [ ] Mobile gesture controls

### Considering
- [ ] Icon pack support
- [ ] Multiple button styles
- [ ] Integration with popular UI libraries
- [ ] Statistics tracking

---

<div align="center">

**Made with ❤️ for the Roblox Community**

[⬆ Back to Top](#-roblox-ui-toggle-button)

</div>

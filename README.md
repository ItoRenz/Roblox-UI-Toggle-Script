# 🎮 Roblox UI Toggle Button

![Roblox](https://img.shields.io/badge/Roblox-Script-00a2ff?style=for-the-badge&logo=roblox&logoColor=white)
![Lua](https://img.shields.io/badge/Lua-5.1-2C2D72?style=for-the-badge&logo=lua&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

A modern, sleek, and customizable UI toggle button for Roblox games. Hide/show all UI elements with a single click while keeping the toggle button always visible.

## ✨ Features

- 🎨 **Modern Design** - Gradient background, glowing effects, and smooth animations
- 📱 **Cross-Platform** - Automatically detects and adapts for PC and Mobile devices
- 🖱️ **Draggable** - Move the button anywhere on your screen
- 💫 **Smooth Animations** - Pulse, breathing, hover, and scale effects
- 🎯 **Smart State Management** - Remembers which UIs were hidden/shown
- 🔄 **Persistent** - Doesn't reset when character respawns
- ⚡ **Lightweight** - Optimized performance with proper cleanup
- 🎨 **Customizable** - Easy to modify colors, sizes, and behavior

## 🚀 Installation

### Method 1: Direct Script
1. Copy the script from `ui-toggle.lua`
2. Paste into a **LocalScript** in `StarterPlayer` → `StarterPlayerScripts`
3. Play the game!

### Method 2: Executor (Client-Side)
1. Copy the entire script
2. Use your preferred Roblox script executor
3. Execute the script

## 🎮 Usage

### Basic Controls
- **Click/Tap** the "UI" button to toggle all UIs on/off
- **Drag** the button to reposition it anywhere on screen
- **Hover** (PC only) for a subtle scale effect

### Visual Indicators
- 🔵 **Blue glow** - UIs are visible
- 🔴 **Red glow** - UIs are hidden
- 💫 **Breathing animation** - Button border pulses slowly when idle

## ⚙️ Configuration

Edit the `SETTINGS` table at the top of the script to customize:

```lua
local SETTINGS = {
	BUTTON_SIZE_PC = UDim2.new(0, 50, 0, 30),      -- PC button size
	BUTTON_SIZE_MOBILE = UDim2.new(0, 60, 0, 35),  -- Mobile button size
	BUTTON_POSITION = UDim2.new(0, 10, 0, 10),     -- Initial position
	ANIMATION_SPEED = 0.3,                          -- Toggle animation speed
	TEXT_VISIBLE = "UI",                            -- Text when UIs visible
	TEXT_HIDDEN = "UI",                             -- Text when UIs hidden
	COLOR_VISIBLE = Color3.fromRGB(100, 200, 255), -- Blue color
	COLOR_HIDDEN = Color3.fromRGB(255, 100, 100),  -- Red color
	ENABLE_DRAGGING = true,                         -- Allow dragging
	SAVE_POSITION = true                            -- Save position (future)
}
```

## 🎨 Customization Examples

### Change Button Size
```lua
BUTTON_SIZE_PC = UDim2.new(0, 70, 0, 40)  -- Larger button
```

### Change Colors
```lua
COLOR_VISIBLE = Color3.fromRGB(0, 255, 0)   -- Green when visible
COLOR_HIDDEN = Color3.fromRGB(255, 165, 0)  -- Orange when hidden
```

### Change Text
```lua
TEXT_VISIBLE = "SHOW"
TEXT_HIDDEN = "HIDE"
```

### Disable Dragging
```lua
ENABLE_DRAGGING = false
```

## 📋 Features Breakdown

### 🎭 Animations
- **Pulse Effect** - Button glows when clicked
- **Breathing Animation** - Border continuously pulses
- **Hover Effect** - Button scales up on mouse hover (PC only)
- **Toggle Scale** - Button shrinks slightly when UIs are hidden

### 🛡️ Safety Features
- **Automatic Cleanup** - Tweens and connections are properly disposed
- **Error Handling** - Gracefully handles deleted UI elements
- **State Preservation** - Remembers original UI states
- **Non-Intrusive** - Doesn't affect game performance

### 📱 Platform Detection
The script automatically detects your platform:
- **PC** - Smaller button, hover effects enabled
- **Mobile** - Larger button, touch-optimized

## 🔧 Technical Details

### Services Used
- `Players` - Player management
- `UserInputService` - Input detection and platform identification
- `TweenService` - Smooth animations
- `RunService` - Frame updates (if needed)

### UI Hierarchy
```
PlayerGui
└── UIToggleGui (ScreenGui)
    └── ToggleButton (Frame)
        ├── UICorner
        ├── UIGradient
        ├── UIStroke
        ├── ShadowStroke
        ├── TextButton
        └── Glow (Frame)
```

## 🐛 Troubleshooting

### Button not appearing?
- Make sure the script is in a **LocalScript**
- Check that it's in `StarterPlayer` → `StarterPlayerScripts`

### Button not hiding certain UIs?
- Some UIs might be protected by the game
- The toggle only affects ScreenGuis in PlayerGui

### Button position resets?
- Position saving is planned but not yet implemented
- You can manually set `BUTTON_POSITION` in settings

## 📝 Changelog

### Version 2.0.0 (Current)
- ✨ Changed icon to "UI" text
- 📏 Reduced button size for both PC and mobile
- 🎨 Improved rectangular button design
- 🔧 Optimized text sizing

### Version 1.0.0
- 🎉 Initial release
- ✨ Basic toggle functionality
- 🎨 Modern UI design
- 📱 Cross-platform support

## 🤝 Contributing

Contributions are welcome! Feel free to:
- Report bugs
- Suggest new features
- Submit pull requests
- Improve documentation

## 📄 License

This project is licensed under the MIT License - see below:

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

If you find this useful, please give it a ⭐!

## 📧 Contact

For questions or suggestions, feel free to open an issue on GitHub.

---

**Made with ❤️ for the Roblox Community**

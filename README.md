# 👁️ Roblox UI Toggle Script

A modern, feature-rich UI toggle button for Roblox games with smooth animations, drag-and-drop functionality, and cross-platform support.

![Roblox](https://img.shields.io/badge/Roblox-000000?style=for-the-badge&logo=roblox&logoColor=white)
![Lua](https://img.shields.io/badge/Lua-2C2D72?style=for-the-badge&logo=lua&logoColor=white)

## ✨ Features

- 🎯 **One-Click UI Toggle** - Hide/show all UI elements with a single button
- 📱 **Cross-Platform Support** - Optimized for both PC and Mobile devices
- 🎨 **Modern Design** - Gradient backgrounds, glow effects, and smooth animations
- 🖱️ **Drag & Drop** - Reposition the button anywhere on screen
- 💾 **State Management** - Remembers which UIs were enabled/disabled
- ⚡ **Performance Optimized** - Proper memory management and tween cleanup
- 🎭 **Visual Feedback** - Color changes, pulse effects, and hover animations
- 🔒 **Persistent** - Button remains visible even after character respawn

## 📸 Preview

```
Normal State: 👁️ (Blue)
Hidden State: 👁️‍🗨️ (Red)
```

The button features:
- Breathing animation effect
- Hover scaling (PC only)
- Click pulse effect
- Smooth color transitions

## 🚀 Installation

### Method 1: Direct Script
1. Open Roblox Studio
2. Insert a **LocalScript** into `StarterPlayer > StarterPlayerScripts`
3. Copy and paste the code from `ui-toggle.lua`
4. Play test your game!

### Method 2: Model Import
1. Download the `.rbxm` model file
2. Right-click in Roblox Studio Explorer
3. Select "Insert from File"
4. Choose the downloaded file

## 📋 Usage

Once installed, the toggle button will automatically appear in the top-left corner when you play the game.

### Controls
- **Click/Tap**: Toggle UI visibility
- **Hold & Drag**: Move the button to a new position
- **Hover** (PC only): Button scales up slightly

### What Gets Hidden?
- All ScreenGui elements except the toggle button itself
- Chat, leaderboard, inventory, and any custom UIs
- The button remembers the original state of each UI

## ⚙️ Configuration

You can customize the script by modifying the `SETTINGS` table:

```lua
local SETTINGS = {
    -- Button sizes
    BUTTON_SIZE_PC = UDim2.new(0, 50, 0, 50),
    BUTTON_SIZE_MOBILE = UDim2.new(0, 70, 0, 70),
    
    -- Default position
    BUTTON_POSITION = UDim2.new(0, 10, 0, 10),
    
    -- Animation speed (seconds)
    ANIMATION_SPEED = 0.3,
    
    -- Icons
    ICON_VISIBLE = "👁️",
    ICON_HIDDEN = "👁️‍🗨️",
    
    -- Colors
    COLOR_VISIBLE = Color3.fromRGB(100, 200, 255),  -- Blue
    COLOR_HIDDEN = Color3.fromRGB(255, 100, 100),   -- Red
    
    -- Features
    ENABLE_DRAGGING = true,
    SAVE_POSITION = true
}
```

## 🎨 Customization Examples

### Change Colors
```lua
COLOR_VISIBLE = Color3.fromRGB(0, 255, 0),   -- Green
COLOR_HIDDEN = Color3.fromRGB(255, 255, 0),  -- Yellow
```

### Change Icons
```lua
ICON_VISIBLE = "🔓",  -- Unlocked
ICON_HIDDEN = "🔒",   -- Locked
```

### Adjust Button Size
```lua
BUTTON_SIZE_PC = UDim2.new(0, 80, 0, 80),      -- Bigger
BUTTON_SIZE_MOBILE = UDim2.new(0, 100, 0, 100), -- Much bigger
```

### Disable Dragging
```lua
ENABLE_DRAGGING = false,
```

## 🛠️ Technical Details

### Services Used
- `Players` - Player detection
- `UserInputService` - Input handling and platform detection
- `TweenService` - Smooth animations
- `RunService` - Performance optimization

### Platform Detection
```lua
local isMobile = UserInputService.TouchEnabled and not UserInputService.KeyboardEnabled
```

### Memory Management
- Active tweens are tracked and cleaned up properly
- Resources are destroyed when player leaves
- No memory leaks from infinite loops

## 🐛 Known Issues

None currently! If you find a bug, please [open an issue](../../issues).

## 📝 Changelog

### Version 2.0.0 (Current)
- ✅ Added drag-and-drop functionality
- ✅ Fixed memory leak in breathing animation
- ✅ Improved tween cleanup system
- ✅ Added safe state restoration
- ✅ Better hover effects for PC
- ✅ Centralized settings configuration
- ✅ Added proper cleanup on player leave

### Version 1.0.0
- Initial release
- Basic toggle functionality
- Cross-platform support
- Visual effects and animations

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 💖 Support

If you find this script useful, please consider:
- ⭐ Starring this repository
- 🐛 Reporting bugs
- 💡 Suggesting new features
- 📢 Sharing with other developers

## 👤 Author

Created with ❤️ for the Roblox development community

## 🔗 Links

- [Roblox Developer Hub](https://create.roblox.com/docs)
- [Roblox DevForum](https://devforum.roblox.com/)

---

**Note**: This script is for educational purposes. Make sure to follow Roblox's Terms of Service and Community Standards when using it in your games.

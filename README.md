# Roblox UI Toggle Button

A compact, draggable UI toggle button for Roblox that allows players to hide and show all GUI elements with a single click.

## Author

**ItoRenz00**

## Features

✨ **Cross-Platform Support** - Works seamlessly on both PC and Mobile devices

🎨 **Modern Design** - Sleek, minimalist design with smooth animations

🖱️ **Draggable** - Move the button anywhere on your screen

💾 **State Management** - Remembers which UIs were visible/hidden

🎭 **Smooth Animations** - Beautiful transitions and effects

🧹 **Auto Cleanup** - Properly cleans up resources when not needed

## Installation

### Method 1: Direct Copy

1. Copy the script from `ui_toggle.lua`
2. In Roblox Studio, insert a `LocalScript` into `StarterPlayer > StarterPlayerScripts`
3. Paste the code into the LocalScript
4. Test in-game!

### Method 2: Load from GitHub (Advanced)

```lua
loadstring(game:HttpGet("YOUR_RAW_GITHUB_URL_HERE"))()
```

**Note:** This requires HTTP requests to be enabled in your game settings.

## Configuration

You can customize the toggle button by modifying the `SETTINGS` table at the top of the script:

```lua
local SETTINGS = {
    -- Button Size
    BUTTON_SIZE_PC = UDim2.new(0, 35, 0, 22),
    BUTTON_SIZE_MOBILE = UDim2.new(0, 45, 0, 28),
    BUTTON_POSITION = UDim2.new(0, 10, 0, 10),
    
    -- Animation
    ANIMATION_SPEED = 0.3,
    
    -- Text
    TEXT_VISIBLE = "UI",
    TEXT_HIDDEN = "UI",
    
    -- Colors
    COLOR_VISIBLE = Color3.fromRGB(100, 200, 255),  -- Blue
    COLOR_HIDDEN = Color3.fromRGB(255, 100, 100),   -- Red
    
    -- Features
    ENABLE_DRAGGING = true,
    SAVE_POSITION = true
}
```

## Usage

### Basic Usage

1. **Click the button** - Toggles all UI elements on/off
2. **Drag the button** - Click and hold to move it around your screen
3. **Hover effect** (PC only) - Button grows slightly when you hover over it

### States

- **Blue Border** - UIs are visible
- **Red Border** - UIs are hidden

## How It Works

1. **Toggle Function**: When clicked, the button saves the state of all ScreenGuis and toggles their visibility
2. **State Restoration**: When toggling back, it restores each UI to its previous state
3. **Smart Detection**: Automatically detects mobile vs PC and adjusts accordingly
4. **Animation System**: Uses TweenService for smooth, professional animations

## Technical Details

### Services Used

- `Players` - Player management
- `UserInputService` - Input detection and platform detection
- `TweenService` - Smooth animations
- `RunService` - Frame-by-frame updates (for dragging)

### Key Functions

- `toggleUI()` - Main function to hide/show all UIs
- `saveUIStates()` - Saves current state of all GUIs
- `restoreUIStates()` - Restores GUIs to saved state
- `createPulseEffect()` - Creates visual feedback animation
- `cleanupTweens()` - Properly disposes of animations

## Compatibility

- ✅ Works on PC (Desktop)
- ✅ Works on Mobile (Touch devices)
- ✅ Works on Tablet
- ✅ Compatible with all Roblox UI elements
- ✅ Respects FilteringEnabled

## Troubleshooting

### Button doesn't appear

- Make sure the script is in a `LocalScript`
- Check that it's placed in `StarterPlayer > StarterPlayerScripts`
- Verify that the player has loaded properly

### Button doesn't hide some UIs

- Some core Roblox UIs cannot be hidden
- Custom UIs must be in `PlayerGui` to be affected
- Check that the UI is a `ScreenGui` instance

### Dragging doesn't work

- Ensure `ENABLE_DRAGGING` is set to `true` in settings
- Make sure the button's parent frame has `Active` set to true

## Customization Examples

### Change Button Position (Top Right)

```lua
BUTTON_POSITION = UDim2.new(1, -50, 0, 10)
```

### Make Button Larger

```lua
BUTTON_SIZE_PC = UDim2.new(0, 60, 0, 40)
BUTTON_SIZE_MOBILE = UDim2.new(0, 70, 0, 50)
```

### Change Colors (Purple Theme)

```lua
COLOR_VISIBLE = Color3.fromRGB(138, 43, 226)
COLOR_HIDDEN = Color3.fromRGB(255, 20, 147)
```

### Disable Dragging

```lua
ENABLE_DRAGGING = false
```

## Performance

- **Lightweight**: Minimal resource usage
- **Optimized**: Uses efficient state management
- **Clean**: Proper garbage collection and cleanup

## Version History

### v1.0.0 (2025)
- Initial release
- Cross-platform support
- Draggable button
- State management
- Smooth animations

## License

This script is free to use and modify for your Roblox projects.

## Contributing

Feel free to fork, modify, and improve this script! If you have suggestions or find bugs, please open an issue.

## Credits

**Author:** ItoRenz00

## Support

If you need help or have questions, feel free to reach out!

---

⭐ If you find this useful, consider giving it a star!

Made with ❤️ by ItoRenz00

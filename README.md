# Screen Filter - Native macOS App

A native macOS application that creates a transparent color filter overlay with adjustable opacity and frequency-based color alternation.

## Features

- **Transparent Overlay**: Stays on top of all windows with adjustable transparency
- **Color Alternation**: Switch between two colors at frequencies from 0-20 Hz
- **Always On Top**: Floats above all other applications
- **Menu Bar Integration**: Quick access from the menu bar
- **Draggable Window**: Reposition anywhere on screen
- **Full Screen Mode**: Expand to cover entire screen
- **Quick Presets**: One-click frequency settings (0, 1, 2, 5, 8, 10, 15, 20 Hz)

## Installation

### Method 1: Direct Installation

1. Copy the `ScreenFilter.app` folder to your `/Applications` directory
2. Double-click `ScreenFilter.app` to launch
3. If macOS shows a security warning:
   - Go to System Preferences → Security & Privacy → General
   - Click "Open Anyway" next to the ScreenFilter message

### Method 2: Run from Terminal

```bash
# Navigate to the app directory
cd /path/to/ScreenFilter.app/Contents/MacOS

# Run the executable
./ScreenFilter
```

### Method 3: Build from Source (Requires Xcode)

If you want to compile it properly with code signing:

1. Install Xcode from the App Store
2. Open Terminal and run:

```bash
# Create a proper Xcode project
mkdir ScreenFilterProject && cd ScreenFilterProject
swift package init --type executable
```

3. Replace the generated code with the Swift source from `ScreenFilter.app/Contents/MacOS/ScreenFilter`
4. Build with: `swift build -c release`

## Usage

### Basic Operation

1. **Launch the app** - The filter window will appear with a control panel
2. **Adjust Opacity** - Use the slider to control transparency (0-100%)
3. **Set Colors** - Click the color pickers to choose your filter colors
4. **Set Frequency** - Adjust how fast colors alternate (0 Hz = static)
5. **Drag Window** - Click and drag to reposition the window

### Controls

- **Opacity Slider**: Controls how transparent the filter is
- **Frequency Slider**: Sets alternation speed (0-20 Hz)
- **Color Pickers**: Choose the two colors to alternate between
- **Preset Buttons**: Quick access to common frequencies
- **Full Screen Button**: Expand filter to entire screen
- **Reset Button**: Return all settings to defaults
- **Hide/Show Button**: Toggle control panel visibility (top-right corner)

### Menu Bar

The app adds a 🎨 icon to your menu bar with these options:
- **Show Window**: Display the filter window
- **Hide Window**: Hide the filter window
- **Quit Screen Filter**: Exit the application

### Keyboard Shortcuts

- `⌘Q` - Quit application
- `⌘S` - Show window (from menu bar)
- `⌘H` - Hide window (from menu bar)

## Use Cases

- **Eye Strain Relief**: Apply a warm tint to reduce blue light
- **Color Temperature Adjustment**: Simulate different lighting conditions
- **Visual Effects**: Create flashing or alternating color effects
- **Screen Tinting**: Apply consistent color filters for photo/video work
- **Accessibility**: Adjust colors for visual impairments
- **Testing**: Simulate color blindness or display issues

## Tips

1. **Lower opacity** (20-40%) works best for seeing content underneath
2. **Use low frequencies** (1-2 Hz) for subtle effects
3. **Hide controls** (top-right button) for minimal interference
4. **Position window** carefully to avoid covering important UI elements
5. **Menu bar access** allows quick hiding when not needed

## Troubleshooting

### App won't open
- Right-click the app → "Open" → "Open" again (bypasses Gatekeeper)
- Check Security & Privacy settings and click "Open Anyway"
- Try running from Terminal (see Method 2 above)

### Window doesn't stay on top
- This is built into the app - if it's not working, try restarting the app
- Make sure you're not in Full Screen mode with another app

### Colors not changing
- Check that frequency is set above 0 Hz
- Try clicking a preset button to reset the frequency
- Make sure the app is running (check menu bar for 🎨 icon)

### Performance issues
- Lower the frequency (high frequencies like 20 Hz can be intensive)
- Close other applications to free up resources
- Reduce window size if covering entire screen

## Technical Details

- **Built with**: Swift, Cocoa, WebKit
- **Minimum macOS**: 10.13 (High Sierra)
- **Window Level**: Floating (stays above most windows)
- **Transparency**: Full alpha channel support
- **Collection Behavior**: Can join all spaces, full screen auxiliary

## Privacy & Permissions

This app does not:
- Collect any data
- Require internet connection
- Access your files or personal information
- Record screen content

The app only displays a colored overlay on your screen.

## Known Limitations

- Cannot overlay above system alerts or password prompts (macOS security feature)
- May not work correctly with some full-screen games
- Screen recording tools may not capture the overlay correctly
- Some color combinations may cause eye strain at high frequencies

## Future Enhancements

Potential features for future versions:
- [ ] Save/load color presets
- [ ] Gradient filters
- [ ] Schedule-based automatic adjustments
- [ ] Multi-monitor support
- [ ] Keyboard shortcuts for opacity/frequency
- [ ] Custom frequency patterns

## License

This software is provided as-is for personal use.

## Support

For issues or questions:
1. Check the Troubleshooting section above
2. Verify you're running macOS 10.13 or later
3. Try resetting to defaults (Reset button)
4. Restart the application

---

**Version**: 1.0  
**Last Updated**: December 2024

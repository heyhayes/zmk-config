# ZMK Configuration for Cradio (Sweep) 34-Key Split Keyboard

This repository contains my personal ZMK firmware configuration for the Cradio (also known as Sweep), a minimal 34-key split keyboard. This configuration features multiple layout options (Colemak-DH, Graphite, QWERTY), chordal hold for home row mods, and sophisticated layer management designed for maximum typing efficiency.

## About the Cradio/Sweep

The Cradio is an open-source 34-key split keyboard designed by David Philip Barr (@davidphilipbarr). It features:
- 3x5 column layout + 2 thumb keys per hand (34 total)
- Direct pin connection (no diodes required)
- Wireless capability via nice!nano controllers
- Minimal, low-profile design

## Why This Configuration?

This keymap is the result of extensive iteration to achieve:
- **Multiple layout options** (Colemak-DH, Graphite, QWERTY) with dynamic switching
- **Chordal hold** home row mods preventing same-hand misfiring
- **One-shot layers** for efficient symbol and number access
- **50/50 hand balance** optimization with modern layouts
- **Programming-focused** symbol arrangement

## Layout Philosophy

The keymap supports multiple base layouts with 8 total layers, chordal hold home row mods, one-shot layers, and dynamic layout switching.

### Key Features
- **Multiple base layouts**: Colemak-DH (default), Graphite, QWERTY
- **Chordal hold home row mods** with opposite-hand rule preventing misfiring
- **One-shot layers** for punctuation and numbers
- **Dynamic layout switching** from arrows layer
- **Mouse support** with movement and scroll
- **Media controls** and brightness controls

## Layer Access

### Thumb Keys:
- **Left inner**: Ctrl/Escape mod-tap
- **Left outer**: Shift/Enter mod-tap  
- **Right inner**: Shift/Space mod-tap
- **Right outer**: One-shot punctuation layer

### Layer Navigation:
- **Arrows layer**: From punctuation layer
- **Numbers layer**: One-shot from punctuation layer
- **Mouse layer**: From arrows layer
- **Layout switching**: From arrows layer (Colemak/Graphite/QWERTY)

### Home Row Mods (Chordal Hold):
- **Left hand**: Alt (S), Gui (T) - only trigger with right hand keys
- **Right hand**: Gui (N), Alt (E) - only trigger with left hand keys

## Complete Layer Layouts

### BASE Layer (0) - Colemak-DH (Default)
```
┌───┬───┬───┬───┬───┐   ┌───┬───┬───┬───┬───┐
│ Q │ W │ F │ P │ B │   │ J │ L │ U │ Y │BSP│
├───┼───┼───┼───┼───┤   ├───┼───┼───┼───┼───┤
│ A │ R │SA │TG │ G │   │ M │NG │AE │ I │ O │
├───┼───┼───┼───┼───┤   ├───┼───┼───┼───┼───┤
│ Z │ X │ C │ D │ V │   │ K │ H │ , │ . │ / │
└───┴───┴───┼───┼───┤   ├───┼───┼───┴───┴───┘
            │CE │SE │   │SS │PU │
            └───┴───┘   └───┴───┘
```
*SA=S+Alt, TG=T+Gui, NG=N+Gui, AE=A+Alt (chordal hold)*
*CE=Ctrl/Esc, SE=Shift/Enter, SS=Shift/Space, PU=Punct(osl)*

### GRAPHITE Layer (8) - Alternative Layout
```
┌───┬───┬───┬───┬───┐   ┌───┬───┬───┬───┬───┐
│ B │ L │ D │ W │ Z │   │ ' │ F │ O │ U │ J │
├───┼───┼───┼───┼───┤   ├───┼───┼───┼───┼───┤
│ N │ R │TA│ SG│ G │   │ Y │HG │AE │ E │ I │
├───┼───┼───┼───┼───┤   ├───┼───┼───┼───┼───┤
│ Q │ X │ M │ C │ V │   │ K │ P │ , │ . │ / │
└───┴───┴───┼───┼───┤   ├───┼───┼───┴───┴───┘
            │CE │SE │   │SS │PU │
            └───┴───┘   └───┴───┘
```
*Optimized for hand alternation and reduced same-finger bigrams*

### SHIFT Layer (1) - Shifted Characters
```
┌───┬───┬───┬───┬───┐   ┌───┬───┬───┬───┬───┐
│ Q │ W │ F │ P │ B │   │ J │ L │ U │ Y │BSP│
├───┼───┼───┼───┼───┤   ├───┼───┼───┼───┼───┤
│ A │ R │ S │ T │ G │   │ M │ N │ E │ I │ O │
├───┼───┼───┼───┼───┤   ├───┼───┼───┼───┼───┤
│ Z │ X │ C │ D │ V │   │ K │ H │ < │ > │ ? │
└───┴───┴───┼───┼───┤   ├───┼───┼───┴───┴───┘
            │   │   │   │   │   │
            └───┴───┘   └───┴───┘
```
*All letters are shifted (uppercase), special characters on bottom right*

### EXTEND Layer (2) - Navigation & Modifiers
```
┌───┬───┬───┬───┬───┐   ┌───┬───┬───┬───┬───┐
│ESC│   │   │   │   │   │PGU│HOM│ ↑ │END│BSP│
├───┼───┼───┼───┼───┤   ├───┼───┼───┼───┼───┤
│ALT│GUI│SHF│CTL│ALT│   │PGD│ ← │ ↓ │ → │DEL│
├───┼───┼───┼───┼───┤   ├───┼───┼───┼───┼───┤
│C-Z│C-X│C-C│GUI│C-V│   │INS│TAB│   │   │RET│
└───┴───┴───┼───┼───┤   ├───┼───┼───┴───┴───┘
            │   │   │   │   │   │
            └───┴───┘   └───┴───┘
```
*One-shot modifiers on left hand, navigation cluster on right*

### SYMBOLS Layer (3) - Programming Symbols
```
┌───┬───┬───┬───┬───┐   ┌───┬───┬───┬───┬───┐
│ ! │ @ │ # │ $ │ % │   │ & │ ( │ ) │ _ │BSP│
├───┼───┼───┼───┼───┤   ├───┼───┼───┼───┼───┤
│ALT│GUI│SHF│CTL│ALT│   │ | │ [ │ ] │ - │ ; │
├───┼───┼───┼───┼───┤   ├───┼───┼───┼───┼───┤
│ ` │ ~ │ ' │ " │ : │   │ \ │ { │ } │ + │ = │
└───┴───┴───┼───┼───┤   ├───┼───┼───┴───┴───┘
            │   │   │   │   │   │
            └───┴───┘   └───┴───┘
```
*Common programming symbols and punctuation*

### NUMBERS Layer (4) - Numpad Layout
```
┌───┬───┬───┬───┬───┐   ┌───┬───┬───┬───┬───┐
│ ! │ @ │ # │ $ │ % │   │ ^ │ 7 │ 8 │ 9 │ + │
├───┼───┼───┼───┼───┤   ├───┼───┼───┼───┼───┤
│ALT│GUI│SHF│CTL│ALT│   │ * │ 4 │ 5 │ 6 │ - │
├───┼───┼───┼───┼───┤   ├───┼───┼───┼───┼───┤
│   │   │   │   │   │   │ 0 │ 1 │ 2 │ 3 │ = │
└───┴───┴───┼───┼───┤   ├───┼───┼───┴───┴───┘
            │   │   │   │   │   │
            └───┴───┘   └───┴───┘
```
*Traditional numpad on right hand with operators*

### FUNCTION Layer (5) - Media & Bluetooth
```
┌───┬───┬───┬───┬───┐   ┌───┬───┬───┬───┬───┐
│CLR│BT0│BT1│BT2│BT3│   │BR+│ F7│ F8│ F9│F12│
├───┼───┼───┼───┼───┤   ├───┼───┼───┼───┼───┤
│ALT│GUI│SHF│CTL│ALT│   │BR-│ F4│ F5│ F6│F11│
├───┼───┼───┼───┼───┤   ├───┼───┼───┼───┼───┤
│V+ │V- │MUT│NXT│PRV│   │P/P│ F1│ F2│ F3│F10│
└───┴───┴───┼───┼───┤   ├───┼───┼───┴───┴───┘
            │   │   │   │   │   │
            └───┴───┘   └───┴───┘
```
*Bluetooth controls, media keys, brightness, and F-keys*

### Legend:
- **CLR**: Bluetooth clear
- **BT0-3**: Bluetooth profile select
- **BR+/-**: Brightness up/down
- **V+/-**: Volume up/down
- **MUT**: Mute
- **NXT/PRV**: Next/Previous track
- **P/P**: Play/Pause
- **C-X**: Ctrl+X (Cut/Copy/Paste/Undo shortcuts)

## Technical Implementation Details

### Custom Behaviors

#### Hold-Tap Configuration
The keymap uses ZMK's hold-tap behavior for dual-function keys:

- **Extend/Escape** (Left outer thumb): Hold-preferred dual function
  - Tap: Escape
  - Hold: Extend layer
  - Configured with 200ms tapping term and 125ms quick-tap

- **Ctrl/Enter** (Left inner thumb): Hold-preferred dual function
  - Tap: Enter
  - Hold: Control modifier
  - Hold-preferred means it favors the hold action when pressed with other keys
  - Configured with 200ms tapping term and 125ms quick-tap

- **Shift/Space** (Right inner thumb): Hold-preferred dual function
  - Tap: Space
  - Hold: Shift layer
  - Provides symmetric shift access from both hands
  - Configured with 200ms tapping term and 125ms quick-tap

#### One-Shot Modifiers
Custom one-shot modifier behaviors provide comfortable modifier access without holding:

```
os_shift, os_ctrl, os_alt, os_gui
```

- **Implementation**: Custom hold-tap behaviors with tap-preferred flavor
- **Tapping term**: 200ms
- **Available on**: Extend, Symbols, Numbers, and Function layers
- **Usage**: Tap once to apply modifier to next key press
- **Benefit**: Reduces pinky strain and awkward key combinations

### Combo Configuration

Two combos provide access to additional layers:

1. **Numbers Layer**: Inner thumb keys (positions 31+32)
   - Left Ctrl/Enter + Right Shift/Space
   - 50ms timeout

2. **Function Layer**: Outer thumb keys (positions 30+33)
   - Left Extend/Escape + Right Symbols
   - 50ms timeout

### Building the Firmware

This configuration uses GitHub Actions for automated builds:

1. Fork this repository
2. Enable GitHub Actions in your fork
3. Make your changes and commit
4. GitHub Actions will build the firmware automatically
5. Download the firmware artifacts from the Actions tab

Local building requires:
- ZMK development environment setup
- West tool for Zephyr
- ARM toolchain

### File Structure

```
zmk-config/
├── config/
│   ├── cradio.keymap    # Main keymap configuration
│   ├── cradio.conf      # Board-specific settings
│   └── west.yml         # West manifest
├── build.yaml           # GitHub Actions build configuration
└── README.md           # This file
```

## Customization Guide

### Changing the Base Layout

To switch from Colemak-DH to another layout (e.g., QWERTY):

1. Edit the `base_layer` bindings in `config/cradio.keymap`
2. Update shifted characters in `shift_layer` if needed
3. Consider adjusting symbol placements for your new layout

### Modifying Layer Access

To change how layers are accessed:

1. **Thumb keys**: Modify the bottom row bindings in `base_layer`
2. **Combos**: Edit combo definitions (timeout-ms, key-positions)
3. **Layer tap**: Use `&lt` behavior for layer-tap functionality

### Adding New Behaviors

Example of adding a new custom behavior:

```devicetree
custom_behavior: custom_behavior {
    compatible = "zmk,behavior-hold-tap";
    label = "CUSTOM_BEHAVIOR";
    #binding-cells = <2>;
    flavor = "tap-preferred";  // or "hold-preferred"
    tapping-term-ms = <200>;
    bindings = <&kp>, <&kp>;
};
```

## Learning Resources

### ZMK Documentation
- [ZMK Official Docs](https://zmk.dev/docs)
- [Behaviors](https://zmk.dev/docs/behaviors/hold-tap)
- [Keymaps](https://zmk.dev/docs/features/keymaps)
- [Combos](https://zmk.dev/docs/features/combos)

### Keyboard Layout Tools
- [Keyboard Layout Editor](http://www.keyboard-layout-editor.com/)
- [Keymapviz](https://github.com/yskoht/keymapviz)

### Community Resources
- [r/ErgoMechKeyboards](https://reddit.com/r/ErgoMechKeyboards)
- [SplitKB Discord](https://splitkb.com/discord)
- [ZMK Discord](https://zmk.dev/community/discord/invite)

## Tips for 34-Key Adaptation

1. **Start with base layer only**: Master typing before adding layers
2. **Practice layer switching**: Use simple exercises to build muscle memory
3. **Customize gradually**: Change one thing at a time
4. **Use combos sparingly**: Too many combos can cause misfires
5. **Consider your use case**: Adapt symbols/numbers to your workflow

## Troubleshooting

### Common Issues

1. **Combos not working**: Check key positions match your matrix
2. **Bluetooth issues**: Ensure `CONFIG_BT` is enabled in `.conf`
3. **Battery drain**: Adjust sleep settings in `.conf` file
4. **Modifier sticky**: Check one-shot behavior timing

### Debugging

Enable ZMK logging in `cradio.conf`:
```
CONFIG_ZMK_USB_LOGGING=y
```

## Contributing

Feel free to:
- Fork and adapt for your own use
- Share your modifications with the community

## License

This configuration is shared under the MIT License. The Cradio hardware design is open source under the CERN Open Hardware License.

## Acknowledgments

- David Philip Barr (@davidphilipbarr) for creating the Cradio/Sweep
- The ZMK contributors and community
- The mechanical keyboard community for layout inspiration

## Related Projects

- [Cradio Hardware](https://github.com/davidphilipbarr/Sweep)
- [ZMK Firmware](https://github.com/zmkfirmware/zmk)
- [Other Cradio Configs](https://github.com/zmkfirmware/zmk/wiki/Community-Repositories#cradio)

---

*Last updated: January 2025*

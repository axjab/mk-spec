# Silakka Field Viper

![Silakka Field Viper](assets/Silakka%20Field%20Viper.svg)

Custom keycap design for the Silakka54 split ergonomic keyboard.

## Reference

- [Supported colors by Yuzu](ref/color-picker.yaml)
- [Yuzu Keycaps](https://yuzukeycaps.com/)

## Palette

```yaml
keyboard:
  model: silakka54
  case:
    material: 3d-printed
    color: charcoal-black

palette:
  name: Field Viper

  base:
    alphas: 802C     # Razer green (existing keycaps)
    mods: 447U       # Charcoal
    accents: 7752U   # Golden khaki

  legends:
    alphas: 442C     # Approximate existing Razer legends
    mods: White      # White on charcoal
    accents: 447U    # Charcoal on golden khaki
```

The palette combines vivid green alphanumeric keys with charcoal modifiers and muted golden-khaki accents. Accent keys identify layer controls and other important functions.

## Font

- **Preferred:** Proxima Nova Soft Bold
- **Fallback:** Noto Sans
- **Design approach:** Icon-first, with text reserved for functions that cannot be communicated clearly through symbols.

## Templates

Templates are configured using Yuzu's native editor.

### 1u — Standard icon

Three-layer template:

1. **Primary icon:** Required, large, centered.
2. **Secondary icon:** Optional, smaller, bottom-right.
3. **Secondary text:** Optional, occupies the same position as the secondary icon.

Only one secondary layer is active at a time.

### 1.25u — Layer key

Dedicated template for thumb-operated layer controls.

### Legend conventions

- Primary legends use the full legend color.
- Secondary legends are visually subordinate.
- Symbols take precedence over text.
- Unused secondary layers are omitted.

*Exact template dimensions and positioning remain subject to final verification in Yuzu.*

## Symbols

Symbols originate from:

1. **MBK Legends** — keyboard-oriented icon assets.
2. [Google Material Symbols](https://fonts.google.com/icons) — preferably the Sharp variant.
3. **Yuzu Icons** — built-in symbols provided by the keycap editor.

Custom SVGs may be imported when the built-in libraries do not provide a suitable symbol.

## Layout

The Silakka54 has 54 programmable keys, including six thumb keys.

### Design principles

- Optimized for programming, terminals, and keyboard-driven window management.
- Dedicated navigation layer, including WASD directional arrows.
- Dedicated symbols and numbers layer.
- Physical arrow keys retained for modifier-heavy window-management shortcuts.
- Standard modifiers remain accessible.
- Frequently used actions take priority over infrequent utilities.
- Generic utility legends allow future firmware remapping.

### Notable conventions

- **Ω:** Symbols layer.
- **Four-direction arrows:** Navigation layer.
- **Heart:** Leader / firmware command key.
- **Tab:** Primary action, with Key Lock as secondary.
- **Alt:** Dedicated thumb modifier.
- **Enter:** Retained in its default bottom-right position.
- **Escape:** Grave Escape behavior, subject to firmware configuration.
- **Brightness and volume:** Dedicated utility controls.

*The detailed per-key firmware mapping is not yet finalized.*

## Cost

**Status:** TBD

Record the final Yuzu quote, shipping, taxes, and total cost in CAD once the order configuration is complete.

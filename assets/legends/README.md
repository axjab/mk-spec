# MBK Legend symbols — Yuzu-compatible SVGs

## Background

These 17 symbols were extracted from the **MBK Legend** icon set associated with [FKcaps](https://fkcaps.com/). They are being reused as symbolic keycap legends in a custom, icon-heavy keyboard design.

The source files contain SVG vector paths. Their visible orientation is not defined by those paths alone: each source also includes a group-level transformation that flips the path vertically and, in one case, shifts it horizontally.

## Why these files were modified

During import into [Yuzu Keycaps](https://yuzukeycaps.com/), the editor was observed to remove the `<g transform="...">` wrapper while retaining the original `<path d="...">` coordinates. This caused imported symbols to appear in a different orientation from the original SVGs.

The issue was diagnosed by comparing the SVG source before and after upload: the post-upload markup contained the same path data but no group transformation. This demonstrates that the visual transformation was lost during that observed import. It does not establish whether every SVG or every future version of Yuzu behaves the same way.

## What changed

Each file was flattened: the original group transformation was applied mathematically to every path point and control point, then the wrapper was removed. The resulting SVG has a single path with coordinates already in their intended positions.

For 16 files, the original transformation was:

```xml
<g transform="scale(1, -1) translate(0 -960)">
```

This maps coordinates `(x, y)` to `(x, 960 - y)`.

For `enter.svg`, the original transformation was:

```xml
<g transform="scale(1, -1) translate(-828 -960)">
```

This maps coordinates `(x, y)` to `(x - 828, 960 - y)`.

The `viewBox="0 0 1024 1024"` is unchanged. Each exported file contains a single `<path>` with `fill="black"` and no transformation attributes. The geometry, including Bézier curve control points, was transformed rather than rasterized.

**Important:** These files retain the *original visual orientation* of the supplied SVGs. They have not been additionally mirrored horizontally.

## Included symbols

`alt`, `backspace`, `break`, `ctrl`, `end`, `enter`, `esc`, `fn`, `home`, `moon`, `numpad-enter`, `numpad-star`, `page-down`, `page-up`, `shift`, `super`, `triangle`.

# Mantle High Contrast Themes Design

## Overview

Add two high contrast theme variants — "Mantle Dark High Contrast" and "Mantle Light High Contrast" — to the existing `themes/mantle.json` file. The themes amplify the originals by removing alpha transparency, pushing background extremes, increasing border visibility, and boosting syntax color saturation/lightness while preserving the same Mantle hue palette and color role assignments.

## Goals

- WCAG AAA (7:1) contrast ratios for primary text against backgrounds
- Increased visual vibrancy and saturation for syntax highlighting
- Full opacity on all text and icon colors (no alpha transparency)
- Maintain the Mantle design system identity — same hues, same structure

## Approach

Pure Opacity + Background Shift: remove all alpha transparency from text/icon colors, push backgrounds to extremes, increase border contrast, and boost syntax color saturation/lightness by ~15-20%. Same hue assignments throughout.

## File Changes

Single file modified: `themes/mantle.json` — two new theme objects appended to the `themes` array after the existing Dark and Light entries.

## Mantle Dark High Contrast

### Backgrounds

| Token | Original | High Contrast |
|-------|----------|---------------|
| background | #121212 | #0a0a0a |
| surface.background | #171717 | #111111 |
| elevated_surface.background | #1c1c1c | #1a1a1a |
| panel.background | #121212 | #0a0a0a |
| editor.background | #121212 | #0a0a0a |
| tab_bar.background | #121212 | #0a0a0a |
| tab.active_background | #171717 | #111111 |
| tab.inactive_background | #121212 | #0a0a0a |
| toolbar.background | #171717 | #111111 |
| status_bar.background | #121212 | #0a0a0a |
| title_bar.background | #121212 | #0a0a0a |
| title_bar.inactive_background | #0e0e0e | #050505 |
| terminal.background | #121212 | #0a0a0a |
| editor.gutter.background | #121212 | #0a0a0a |
| editor.subheader.background | #121212 | #0a0a0a |

### Text & Icons (full opacity)

| Token | Original | High Contrast |
|-------|----------|---------------|
| text | #ffffffb3 | #ffffff |
| text.muted | #ffffff80 | #d4d4d4 |
| text.placeholder | #ffffff66 | #a1a1a1 |
| text.disabled | #ffffff40 | #737373 |
| text.accent | #699afc | #7aabff |
| icon | #ffffffb3 | #ffffff |
| icon.muted | #ffffff80 | #d4d4d4 |
| icon.disabled | #ffffff40 | #737373 |
| icon.accent | #699afc | #7aabff |
| editor.foreground | #ffffffb3 | #ffffff |

### Borders

| Token | Original | High Contrast |
|-------|----------|---------------|
| border | #404040 | #525252 |
| border.variant | #262626 | #404040 |
| border.focused | #3e6ff4 | #5a85ff |
| border.selected | #3e6ff4 | #5a85ff |
| border.disabled | #262626 | #333333 |

### Editor Details

| Token | Original | High Contrast |
|-------|----------|---------------|
| editor.active_line.background | #262626 | #333333 |
| editor.highlighted_line.background | #262626 | #333333 |
| editor.line_number | #525252 | #737373 |
| editor.active_line_number | #ffffff | #ffffff |
| editor.hover_line_number | #a1a1a1 | #d4d4d4 |
| editor.invisible | #404040 | #525252 |
| editor.wrap_guide | #ffffff0d | #ffffff1a |
| editor.active_wrap_guide | #ffffff1a | #ffffff33 |
| editor.indent_guide | #262626 | #404040 |
| editor.indent_guide_active | #404040 | #525252 |
| editor.document_highlight.read_background | #3e6ff41a | #3e6ff433 |
| editor.document_highlight.write_background | #3e6ff433 | #3e6ff455 |
| search.match_background | #3e6ff444 | #3e6ff466 |

### Elements

| Token | Original | High Contrast |
|-------|----------|---------------|
| element.background | #171717 | #111111 |
| element.hover | #262626 | #333333 |
| element.active | #404040 | #525252 |
| element.selected | #262626 | #333333 |
| element.disabled | #171717 | #111111 |
| ghost_element.hover | #262626 | #333333 |
| ghost_element.active | #404040 | #525252 |
| ghost_element.selected | #262626 | #333333 |
| ghost_element.disabled | #17171780 | #111111a0 |

### Scrollbar

| Token | Original | High Contrast |
|-------|----------|---------------|
| scrollbar.thumb.background | #ffffff1a | #ffffff33 |
| scrollbar.thumb.hover_background | #ffffff33 | #ffffff55 |
| scrollbar.thumb.border | #ffffff0d | #ffffff1a |
| scrollbar.track.border | #262626 | #404040 |

### Semantic Colors

| Token | Original | High Contrast |
|-------|----------|---------------|
| error | #fb2c36 | #ff4d55 |
| error.background | #fb2c3620 | #ff4d5530 |
| error.border | #fb2c3666 | #ff4d5588 |
| warning | #f59e0b | #ffb733 |
| warning.background | #f59e0b20 | #ffb73330 |
| warning.border | #f59e0b66 | #ffb73388 |
| success | #22c55e | #3ddb77 |
| success.background | #22c55e20 | #3ddb7730 |
| success.border | #22c55e66 | #3ddb7788 |
| info | #3e6ff4 | #5a85ff |
| info.background | #3e6ff420 | #5a85ff30 |
| info.border | #3e6ff466 | #5a85ff88 |
| hint | #737373 | #8a8a8a |
| hint.background | #73737320 | #8a8a8a30 |
| hint.border | #73737366 | #8a8a8a88 |

### Git Status Colors

| Token | Original | High Contrast |
|-------|----------|---------------|
| created | #22c55e | #3ddb77 |
| modified | #f59e0b | #ffb733 |
| deleted | #fb2c36 | #ff4d55 |
| renamed | #699afc | #7aabff |
| conflict | #f59e0b | #ffb733 |
| ignored | #525252 | #737373 |
| hidden | #525252 | #737373 |
| predictive | #525252 | #737373 |

### Syntax Highlighting

| Token | Original | High Contrast |
|-------|----------|---------------|
| keyword | #699afc | #7aabff |
| function | #699afc | #7aabff |
| function.method | #699afc | #7aabff |
| constructor | #699afc | #7aabff |
| string | #05df72 | #0fff80 |
| string.escape | #05df72 | #0fff80 |
| string.regex | #fdc700 | #ffe033 |
| string.special | #05df72 | #0fff80 |
| comment | #737373 | #8a8a8a |
| comment.doc | #737373 | #8a8a8a |
| number | #7c86ff | #9196ff |
| boolean | #7c86ff | #9196ff |
| constant | #7c86ff | #9196ff |
| type | #699afc | #7aabff |
| type.interface | #699afc | #7aabff |
| enum | #7c86ff | #9196ff |
| variable | #fdc700 | #ffe033 |
| variable.special | #fdc700 | #ffe033 |
| variable.parameter | #fdc700 | #ffe033 |
| property | #7c86ff | #9196ff |
| attribute | #05df72 | #0fff80 |
| tag | #7c86ff | #9196ff |
| operator | #05df72 | #0fff80 |
| punctuation | #ffffffb3 | #ffffff |
| punctuation.bracket | #ffffffb3 | #ffffff |
| punctuation.delimiter | #ffffffb3 | #ffffff |
| punctuation.special | #7c86ff | #9196ff |
| namespace | #ffffffb3 | #ffffff |
| label | #699afc | #7aabff |
| link_text | #699afc | #7aabff |
| link_uri | #05df72 | #0fff80 |
| emphasis | #699afc | #7aabff |
| emphasis.strong | #699afc | #7aabff |
| title | #699afc | #7aabff |
| text.literal | #05df72 | #0fff80 |
| preproc | #699afc | #7aabff |
| embedded | #ffffffb3 | #ffffff |
| primary | #ffffffb3 | #ffffff |
| predictive | #525252 | #737373 |
| hint | #525252 | #737373 |

### Terminal Colors

Boosted bright variants, same hue mapping:

| Token | Original | High Contrast |
|-------|----------|---------------|
| terminal.foreground | #d4d4d4 | #ffffff |
| terminal.bright_foreground | #fafafa | #ffffff |
| terminal.dim_foreground | #737373 | #8a8a8a |
| terminal.ansi.black | #121212 | #0a0a0a |
| terminal.ansi.bright_black | #525252 | #737373 |
| terminal.ansi.dim_black | #0e0e0e | #050505 |
| terminal.ansi.red | #fb2c36 | #ff4d55 |
| terminal.ansi.bright_red | #ff6467 | #ff7a7d |
| terminal.ansi.dim_red | #9f0712 | #b81020 |
| terminal.ansi.green | #22c55e | #3ddb77 |
| terminal.ansi.bright_green | #4ade80 | #66e898 |
| terminal.ansi.dim_green | #166534 | #1e8045 |
| terminal.ansi.yellow | #f59e0b | #ffb733 |
| terminal.ansi.bright_yellow | #fbbf24 | #ffd04d |
| terminal.ansi.dim_yellow | #854d0e | #a06010 |
| terminal.ansi.blue | #3e6ff4 | #5a85ff |
| terminal.ansi.bright_blue | #699afc | #7aabff |
| terminal.ansi.dim_blue | #1f2d89 | #2a3da0 |
| terminal.ansi.magenta | #a855f7 | #bb77ff |
| terminal.ansi.bright_magenta | #c084fc | #d0a0ff |
| terminal.ansi.dim_magenta | #6b21a8 | #7e30c0 |
| terminal.ansi.cyan | #14b8a6 | #20d4c0 |
| terminal.ansi.bright_cyan | #2dd4bf | #50e8d8 |
| terminal.ansi.dim_cyan | #115e59 | #1a7570 |
| terminal.ansi.white | #d4d4d4 | #ffffff |
| terminal.ansi.bright_white | #fafafa | #ffffff |
| terminal.ansi.dim_white | #a1a1a1 | #c4c4c4 |

### Players & Accents

Players use boosted accent colors with higher opacity selections (`#...44` instead of `#...33`):

| Player | Cursor/Background | Selection |
|--------|-------------------|-----------|
| 1 | #5a85ff | #5a85ff44 |
| 2 | #3ddb77 | #3ddb7744 |
| 3 | #ffb733 | #ffb73344 |
| 4 | #bb77ff | #bb77ff44 |
| 5 | #ff4d55 | #ff4d5544 |
| 6 | #20d4c0 | #20d4c044 |

Accents: `#5a85ff`, `#7aabff`, `#3ddb77`, `#ffb733`, `#ff4d55`, `#bb77ff`, `#20d4c0`

### Misc

| Token | Original | High Contrast |
|-------|----------|---------------|
| drop_target.background | #3e6ff430 | #5a85ff44 |
| pane.focused_border | #3e6ff4 | #5a85ff |
| panel.focused_border | #3e6ff4 | #5a85ff |
| link_text.hover | #699afc | #7aabff |

---

## Mantle Light High Contrast

### Backgrounds

| Token | Original | High Contrast |
|-------|----------|---------------|
| background | #fafafa | #ffffff |
| surface.background | #ffffff | #ffffff |
| elevated_surface.background | #ffffff | #ffffff |
| panel.background | #fafafa | #ffffff |
| editor.background | #fafafa | #ffffff |
| tab_bar.background | #fafafa | #ffffff |
| tab.active_background | #ffffff | #ffffff |
| tab.inactive_background | #fafafa | #f5f5f5 |
| toolbar.background | #ffffff | #ffffff |
| status_bar.background | #fafafa | #ffffff |
| title_bar.background | #fafafa | #ffffff |
| title_bar.inactive_background | #f5f5f5 | #fafafa |
| terminal.background | #fafafa | #ffffff |
| editor.gutter.background | #fafafa | #ffffff |
| editor.subheader.background | #fafafa | #ffffff |

### Text & Icons (full opacity)

| Token | Original | High Contrast |
|-------|----------|---------------|
| text | #121212bf | #121212 |
| text.muted | #12121299 | #404040 |
| text.placeholder | #12121280 | #525252 |
| text.disabled | #12121266 | #737373 |
| text.accent | #2e54eb | #1a3fd4 |
| icon | #121212bf | #121212 |
| icon.muted | #12121299 | #404040 |
| icon.disabled | #12121266 | #737373 |
| icon.accent | #2e54eb | #1a3fd4 |
| editor.foreground | #121212bf | #121212 |

### Borders

| Token | Original | High Contrast |
|-------|----------|---------------|
| border | #d4d4d4 | #a1a1a1 |
| border.variant | #e5e5e5 | #c4c4c4 |
| border.focused | #3e6ff4 | #1a3fd4 |
| border.selected | #3e6ff4 | #1a3fd4 |
| border.disabled | #e5e5e5 | #d4d4d4 |

### Editor Details

| Token | Original | High Contrast |
|-------|----------|---------------|
| editor.active_line.background | #f5f5f5 | #f0f0f0 |
| editor.highlighted_line.background | #f0f4ff | #e5ecff |
| editor.line_number | #a1a1a1 | #737373 |
| editor.active_line_number | #121212 | #121212 |
| editor.hover_line_number | #525252 | #333333 |
| editor.invisible | #d4d4d4 | #a1a1a1 |
| editor.wrap_guide | #0000000d | #0000001a |
| editor.active_wrap_guide | #0000001a | #00000033 |
| editor.indent_guide | #e5e5e5 | #c4c4c4 |
| editor.indent_guide_active | #d4d4d4 | #a1a1a1 |
| editor.document_highlight.read_background | #3e6ff41a | #1a3fd433 |
| editor.document_highlight.write_background | #3e6ff433 | #1a3fd455 |
| search.match_background | #3e6ff433 | #1a3fd444 |

### Elements

| Token | Original | High Contrast |
|-------|----------|---------------|
| element.background | #ffffff | #ffffff |
| element.hover | #f5f5f5 | #ebebeb |
| element.active | #e5e5e5 | #d4d4d4 |
| element.selected | #f0f4ff | #e0e8ff |
| element.disabled | #fafafa | #f5f5f5 |
| ghost_element.hover | #f5f5f5 | #ebebeb |
| ghost_element.active | #e5e5e5 | #d4d4d4 |
| ghost_element.selected | #f0f4ff | #e0e8ff |
| ghost_element.disabled | #fafafa80 | #f5f5f5a0 |

### Scrollbar

| Token | Original | High Contrast |
|-------|----------|---------------|
| scrollbar.thumb.background | #0000001a | #00000033 |
| scrollbar.thumb.hover_background | #00000033 | #00000055 |
| scrollbar.thumb.border | #0000000d | #0000001a |
| scrollbar.track.border | #e5e5e5 | #c4c4c4 |

### Semantic Colors

| Token | Original | High Contrast |
|-------|----------|---------------|
| error | #e7000b | #c50008 |
| error.background | #e7000b15 | #c5000825 |
| error.border | #e7000b44 | #c5000866 |
| warning | #d97706 | #b45309 |
| warning.background | #d9770615 | #b4530925 |
| warning.border | #d9770644 | #b4530966 |
| success | #16a34a | #15803d |
| success.background | #16a34a15 | #15803d25 |
| success.border | #16a34a44 | #15803d66 |
| info | #2e54eb | #1a3fd4 |
| info.background | #2e54eb15 | #1a3fd425 |
| info.border | #2e54eb44 | #1a3fd466 |
| hint | #a1a1a1 | #737373 |
| hint.background | #a1a1a115 | #73737325 |
| hint.border | #a1a1a144 | #73737366 |

### Git Status Colors

| Token | Original | High Contrast |
|-------|----------|---------------|
| created | #16a34a | #15803d |
| modified | #d97706 | #b45309 |
| deleted | #e7000b | #c50008 |
| renamed | #2e54eb | #1a3fd4 |
| conflict | #d97706 | #b45309 |
| ignored | #a1a1a1 | #737373 |
| hidden | #a1a1a1 | #737373 |
| predictive | #a1a1a1 | #737373 |

### Syntax Highlighting

| Token | Original | High Contrast |
|-------|----------|---------------|
| keyword | #2e54eb | #1a3fd4 |
| function | #2e54eb | #1a3fd4 |
| function.method | #2e54eb | #1a3fd4 |
| constructor | #2e54eb | #1a3fd4 |
| string | #00a63e | #008a30 |
| string.escape | #00a63e | #008a30 |
| string.regex | #d08700 | #b87400 |
| string.special | #00a63e | #008a30 |
| comment | #737373 | #5c5c5c |
| comment.doc | #737373 | #5c5c5c |
| number | #4f39f6 | #3b28d9 |
| boolean | #4f39f6 | #3b28d9 |
| constant | #4f39f6 | #3b28d9 |
| type | #2e54eb | #1a3fd4 |
| type.interface | #2e54eb | #1a3fd4 |
| enum | #4f39f6 | #3b28d9 |
| variable | #d08700 | #b87400 |
| variable.special | #d08700 | #b87400 |
| variable.parameter | #d08700 | #b87400 |
| property | #4f39f6 | #3b28d9 |
| attribute | #00a63e | #008a30 |
| tag | #4f39f6 | #3b28d9 |
| operator | #00a63e | #008a30 |
| punctuation | #121212bf | #121212 |
| punctuation.bracket | #121212bf | #121212 |
| punctuation.delimiter | #121212bf | #121212 |
| punctuation.special | #4f39f6 | #3b28d9 |
| namespace | #121212bf | #121212 |
| label | #2e54eb | #1a3fd4 |
| link_text | #2e54eb | #1a3fd4 |
| link_uri | #00a63e | #008a30 |
| emphasis | #2e54eb | #1a3fd4 |
| emphasis.strong | #2e54eb | #1a3fd4 |
| title | #2e54eb | #1a3fd4 |
| text.literal | #00a63e | #008a30 |
| preproc | #2e54eb | #1a3fd4 |
| embedded | #121212bf | #121212 |
| primary | #121212bf | #121212 |
| predictive | #a1a1a1 | #737373 |
| hint | #a1a1a1 | #737373 |

### Terminal Colors

| Token | Original | High Contrast |
|-------|----------|---------------|
| terminal.foreground | #404040 | #121212 |
| terminal.bright_foreground | #121212 | #000000 |
| terminal.dim_foreground | #a1a1a1 | #737373 |
| terminal.ansi.black | #121212 | #000000 |
| terminal.ansi.bright_black | #404040 | #333333 |
| terminal.ansi.dim_black | #737373 | #525252 |
| terminal.ansi.red | #e7000b | #c50008 |
| terminal.ansi.bright_red | #fb2c36 | #e7000b |
| terminal.ansi.dim_red | #c10007 | #a00006 |
| terminal.ansi.green | #16a34a | #15803d |
| terminal.ansi.bright_green | #22c55e | #16a34a |
| terminal.ansi.dim_green | #15803d | #166534 |
| terminal.ansi.yellow | #d97706 | #b45309 |
| terminal.ansi.bright_yellow | #f59e0b | #d97706 |
| terminal.ansi.dim_yellow | #b45309 | #854d0e |
| terminal.ansi.blue | #2e54eb | #1a3fd4 |
| terminal.ansi.bright_blue | #3e6ff4 | #2e54eb |
| terminal.ansi.dim_blue | #1e3ad6 | #162fb0 |
| terminal.ansi.magenta | #9333ea | #7e22ce |
| terminal.ansi.bright_magenta | #a855f7 | #9333ea |
| terminal.ansi.dim_magenta | #7e22ce | #6b21a8 |
| terminal.ansi.cyan | #0d9488 | #0a7e73 |
| terminal.ansi.bright_cyan | #14b8a6 | #0d9488 |
| terminal.ansi.dim_cyan | #0f766e | #115e59 |
| terminal.ansi.white | #e5e5e5 | #d4d4d4 |
| terminal.ansi.bright_white | #fafafa | #e5e5e5 |
| terminal.ansi.dim_white | #d4d4d4 | #a1a1a1 |

### Players & Accents

| Player | Cursor/Background | Selection |
|--------|-------------------|-----------|
| 1 | #1a3fd4 | #1a3fd433 |
| 2 | #15803d | #15803d33 |
| 3 | #b45309 | #b4530933 |
| 4 | #7e22ce | #7e22ce33 |
| 5 | #c50008 | #c5000833 |
| 6 | #0a7e73 | #0a7e7333 |

Accents: `#1a3fd4`, `#2e54eb`, `#15803d`, `#b45309`, `#c50008`, `#7e22ce`, `#0a7e73`

### Misc

| Token | Original | High Contrast |
|-------|----------|---------------|
| drop_target.background | #3e6ff430 | #1a3fd444 |
| pane.focused_border | #3e6ff4 | #1a3fd4 |
| panel.focused_border | #3e6ff4 | #1a3fd4 |
| link_text.hover | #2e54eb | #1a3fd4 |

## Unchanged Transparent Tokens

The following tokens remain `#00000000` (fully transparent) in both HC variants, unchanged from the originals:

- `border.transparent`
- `ghost_element.background`
- `scrollbar.track.background`

## Font Style & Weight Inheritance

All `font_style` and `font_weight` values are inherited verbatim from the corresponding original theme and are not repeated in the syntax tables above. The syntax tables specify only color changes. For reference, the inherited styles are:

- `font_style: "italic"` on: comment, comment.doc, type.interface, variable.parameter, emphasis, predictive
- `font_weight: 700` on: emphasis.strong
- `font_weight: 500` on: title

## Light HC Player Selection Opacity

The original Light theme uses `#...26` (~15%) for player selection opacity. The Light HC variant intentionally upgrades this to `#...33` (~20%) for increased visibility, matching the Dark theme's selection opacity pattern.

## What Stays The Same

- Theme JSON structure and schema version (v0.2.0)
- Color role assignments (which hue maps to which syntax element)
- Player count (6) and accent count (7)
- Semantic color roles (error=red, warning=yellow, success=green, info=blue)

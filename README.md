# Obsidian Custom Callouts & Grid Layout

A pair of CSS snippets for [Obsidian](https://obsidian.md) that provide a fully customisable callout system with 10 configurable colour slots and a flexible grid layout system — all controllable via the [Style Settings](https://github.com/obsidian-community/obsidian-style-settings) plugin.

No JavaScript. No community plugins required beyond Style Settings. Works standalone.

---

## Screenshots

> _Add screenshots here once published_

---

## Features

### Custom Callouts (`custom_callouts.css`)

- **10 colour slots** — each fully configurable via Style Settings (background, border, title & icon colour, body text colour)
- **Native Obsidian title style** — coloured icon + title text, matching native callout aesthetics
- **Lucide icon support** — set any [Lucide](https://lucide.dev) icon per slot via Style Settings
- **`no-title` variant** — render a clean card without a heading
- **Global toggles** — transparent background and hidden border toggles per slot via Style Settings
- **Grid system built in** — `[!grid]` callout with 6 layout patterns
- **Table styling** — tables inside callouts render with correct background contrast
- **Responsive** — stacks to single column on narrow screens
- **Light & dark mode** — follows vault theme via CSS variables
- **Standalone** — works without `multi_column_layout.css`

### Multi Column Layout (`multi_column_layout.css`)

- **Flex-based columns** — `[!multi-column]` wraps any content in responsive columns
- **Width controls** — `wide-2` through `wide-4` for proportional sizing
- **Percentage widths** — `w-20` through `w-80` for precise control
- **Height controls** — `h-10` through `h-100` (viewport height units)
- **Blank container** — `[!blank]` for unstyled column content
- **Fixed column layouts** — `two-column` and `three-column` CSS classes via frontmatter `cssclasses`
- **Style Settings integration** — column gap and minimum width configurable

---

## Installation

### Manual

1. Download `custom_callouts.css` and/or `multi_column_layout.css`
2. Place them in your vault's `.obsidian/snippets/` folder
3. Open Obsidian → **Settings → Appearance → CSS Snippets**
4. Enable the snippet(s)

### Style Settings (Recommended)

Install the [Style Settings](https://github.com/obsidian-community/obsidian-style-settings) community plugin to get a full settings panel for colours, icons, border width, corner radius, and more.

**Settings → Style Settings → Custom Callouts**

---

## Usage

### Custom Callout — With Title

```markdown
> [!col|slot-1] My Title
> Content goes here
```

### Custom Callout — No Title

```markdown
> [!col|slot-2 no-title]
> Content without a heading
```

### Custom Callout — Transparent Background

```markdown
> [!col|slot-3 no-title]
> Clean card with no background
```
_(Toggle transparent background for Slot 3 in Style Settings)_

---

## Grid Layouts

All grid layouts use the `[!grid]` callout with a layout modifier. Inner columns use `[!col]` with any slot.

### 2×2 Grid

```markdown
> [!grid|grid-2x2]
>
>> [!col|slot-1 no-title]
>> Top Left
>
>> [!col|slot-2 no-title]
>> Top Right
>
>> [!col|slot-3 no-title]
>> Bottom Left
>
>> [!col|slot-4 no-title]
>> Bottom Right
```

### Left Column Spanning (`grid-1-2`)

```markdown
> [!grid|grid-1-2]
>
>> [!col|slot-1 span no-title]
>> Left — spans both rows
>
>> [!col|slot-2 no-title]
>> Top Right
>
>> [!col|slot-3 no-title]
>> Bottom Right
```

### Right Column Spanning (`grid-2-1`)

```markdown
> [!grid|grid-2-1]
>
>> [!col|slot-1 no-title]
>> Top Left
>
>> [!col|slot-2 span no-title]
>> Right — spans both rows
>
>> [!col|slot-3 no-title]
>> Bottom Left
```

### 3 Equal Columns (`grid-3`)

```markdown
> [!grid|grid-3]
>
>> [!col|slot-1 no-title]
>> Column 1
>
>> [!col|slot-2 no-title]
>> Column 2
>
>> [!col|slot-3 no-title]
>> Column 3
```

### Featured — Large Left (`grid-featured-ll`)

Large left column (2/3) with two stacked right columns (1/3).

```markdown
> [!grid|grid-featured-ll]
>
>> [!col|slot-1 no-title]
>> Main content
>
>> [!col|slot-2 span no-title]
>> Right — spans both rows
>
>> [!col|slot-3 no-title]
>> Secondary
```

### Featured — Large Right (`grid-featured-lr`)

Two stacked left columns (1/3) with a large right column (2/3).

```markdown
> [!grid|grid-featured-lr]
>
>> [!col|slot-1 span no-title]
>> Left — spans both rows
>
>> [!col|slot-2 no-title]
>> Main content
>
>> [!col|slot-3 no-title]
>> Secondary
```

---

## Multi Column Layout

### Basic Two Columns

```markdown
> [!multi-column]
>
>> [!col|slot-1] Left Column
>> Content here
>
>> [!col|slot-2] Right Column
>> Content here
```

### Percentage Width Control

```markdown
> [!multi-column]
>
>> [!col|slot-1 w-25 no-title]
>> Narrow — 25% wide
>
>> [!col|slot-2 no-title]
>> Takes remaining width automatically
```

### Available Width Classes

| Class | Width |
|---|---|
| `w-10` | 10% |
| `w-20` | 20% |
| `w-25` | 25% |
| `w-33` | 33% |
| `w-40` | 40% |
| `w-50` | 50% |
| `w-60` | 60% |
| `w-66` | 66% |
| `w-75` | 75% |
| `w-80` | 80% |

### Available Height Classes

| Class | Height |
|---|---|
| `h-10` | 10vh |
| `h-20` | 20vh |
| `h-25` | 25vh |
| `h-30` | 30vh |
| `h-40` | 40vh |
| `h-50` | 50vh |
| `h-75` | 75vh |
| `h-100` | 100vh |

---

## Slot Quick Reference

| Slot | Usage | With Title | No Title |
|---|---|---|---|
| Slot 1 | `[!col\|slot-1]` | ✅ | `[!col\|slot-1 no-title]` |
| Slot 2 | `[!col\|slot-2]` | ✅ | `[!col\|slot-2 no-title]` |
| Slot 3 | `[!col\|slot-3]` | ✅ | `[!col\|slot-3 no-title]` |
| Slot 4 | `[!col\|slot-4]` | ✅ | `[!col\|slot-4 no-title]` |
| Slot 5 | `[!col\|slot-5]` | ✅ | `[!col\|slot-5 no-title]` |
| Slot 6 | `[!col\|slot-6]` | ✅ | `[!col\|slot-6 no-title]` |
| Slot 7 | `[!col\|slot-7]` | ✅ | `[!col\|slot-7 no-title]` |
| Slot 8 | `[!col\|slot-8]` | ✅ | `[!col\|slot-8 no-title]` |
| Slot 9 | `[!col\|slot-9]` | ✅ | `[!col\|slot-9 no-title]` |
| Slot 10 | `[!col\|slot-10]` | ✅ | `[!col\|slot-10 no-title]` |

---

## Grid Layout Reference

| Layout | Modifier | Description |
|---|---|---|
| 2×2 Grid | `grid-2x2` | 2 equal columns, 2 equal rows |
| Left Spanning | `grid-1-2` | Left column spans 2 rows |
| Right Spanning | `grid-2-1` | Right column spans 2 rows |
| 3 Columns | `grid-3` | 3 equal columns |
| Featured Left | `grid-featured-ll` | Large left (2/3) + 2 stacked right (1/3) |
| Featured Right | `grid-featured-lr` | 2 stacked left (1/3) + large right (2/3) |

Add `span` to any `[!col]` metadata to make it span rows in supported layouts.

---

## Style Settings

With [Style Settings](https://github.com/obsidian-community/obsidian-style-settings) installed, you get full control over:

**Custom Callouts:**
- Column & grid gap
- Border width (slider 0–5px)
- Corner radius (slider 0–20px)
- Per slot: icon (any Lucide icon name), transparent background toggle, hide border toggle, background colour, border colour, title & icon colour, body text colour

**Multi Column Layout:**
- Column gap
- Minimum column width before stacking

All colour pickers support separate light and dark mode values.

---

## Compatibility

- **Obsidian** 1.0+
- **Recommended:** [Style Settings](https://github.com/obsidian-community/obsidian-style-settings) plugin
- Works with all community themes
- Tested in Reading View and Live Preview

---

## Notes

- The `[!grid]` system requires `custom_callouts.css` — it is self-contained
- `multi_column_layout.css` is optional — add it for flex-based multi-column layouts alongside the grid system
- Both files can be enabled independently
- All grid and callout layouts render correctly in **Reading View**; Live Preview may show source for complex nested callouts

---

## Contributing

Issues and PRs welcome. If you've built something interesting with these snippets, feel free to share a screenshot in the issues tab.

---

## Licence

MIT © [AI Centra LTD](https://github.com/aicentra)

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

# Obsidian Custom Callouts & Grid Layout

A pair of CSS snippets for [Obsidian](https://obsidian.md) that provide a fully customisable callout system with 10 configurable colour slots and a flexible grid layout system, all controllable via the [Style Settings](https://github.com/obsidian-community/obsidian-style-settings) plugin.

No JavaScript. No community plugins required beyond Style Settings. Works standalone.

---


## Grid Layout Examples:

![Screen shot of grid layout](https://github.com/user-attachments/assets/ed3115b3-8562-4aca-8565-3c609fbc6a8c)


## Callout Examples:

<img width="1899" height="990" alt="Screenshot 2026-05-14 at 03 31 23" src="https://github.com/user-attachments/assets/e325595c-7c24-4de5-9702-5a8d952d4479" />



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

---

## Installation

### Manual

1. Download `custom_callouts.css`
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


<img width="784" height="912" alt="Screenshot 2026-05-14 at 03 33 49" src="https://github.com/user-attachments/assets/6c87866a-89ef-4393-b70c-b721b5b3e7e3" />





---

## Compatibility

- **Obsidian** 1.0+
- **Recommended:** [Style Settings](https://github.com/obsidian-community/obsidian-style-settings) plugin
- Works with all community themes
- Tested in Reading View and Live Preview

---

## Notes

- The `[!grid]` system is self-contained
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

---

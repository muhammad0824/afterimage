# Design

The photo is the only color on screen. The interface is concrete, paper and ink, modeled on the references the owner chose: Rick Owens (pale concrete ground, objects floating on it), SSENSE (uppercase grotesk labels, Times-style serif copy, hairlines, square corners) and Figma (one solid black action).

## Tokens

| Token | Value | Use |
|---|---|---|
| `--ground` | `#d4d3d0` | Stage behind the photo. Mid-gray so colors are judged neither too bright nor too dark |
| `--paper` | `#f3f2ef` | Header, panel, dialogs, select fields |
| `--paper-2` | `#e9e8e4` | Empty thumbnails, icon-button hover |
| `--ink` | `#121211` | Text, primary button, switches, slider fill, selection. The only accent |
| `--ink-2` | `#464542` | Control labels, inactive effect names |
| `--ink-3` | `#6b6a66` | Hints and metadata (4.9:1 on paper) |
| `--rule` / `--rule-2` | ink at 14% / 28% | Hairlines, slider track, field borders |

No hue appears in the interface. Status is shown by ink and motion, never by green or amber.

## Type

- **Schibsted Grotesk** (400–700) for everything functional. Labels, buttons, section heads and effect names are uppercase, 11–12px, tracked .08–.12em, weight 600. Control labels and values are 13px sentence case; values use tabular numerals.
- **Tinos** (Times-metric serif) for hints, section notes and dialog copy, 15–16px, in `--ink-3`. It plays the part of SSENSE's serif product copy.
- Wordmark: AFTERIMAGE, uppercase, tracked .16em, 19px on phones and 22px on desktop.

## Shape and depth

- Square corners everywhere. The only round shape is the slider thumb, kept for touch.
- 1px hairlines separate groups. There are no cards: the effect stack is a ruled list, indented under its running-order number.
- One shadow: the photo floats on the ground (`0 18px 40px -18px`). Dialogs use the same soft offset shadow.

## Components

- **Buttons:** 36px, 1px ink border, uppercase 11px. Primary is solid ink. Bare buttons are text that underlines on hover.
- **Toolbar under the photo:** text-only uppercase actions (Surprise me, Add layers, Bigger, Compare) with a 6px ink status square at the end.
- **Switch:** square, outlined in ink; on fills ink with a paper knob.
- **Slider:** 2px track, ink fill up to the value, 18px ink thumb ringed in paper.
- **Recipes:** 4:5 thumbnails. Selected gets a 1.5px ink outline and an underlined name.
- **Toast:** solid ink rectangle, paper text.

## Motion

One signature: while the image renders, a 2px ink hairline sweeps along the top edge of the stage (`cubic-bezier(.16, 1, .3, 1)`). With reduced motion it becomes a static faint line. Everything else is short ease-out color and position changes.

## Layout

- **Phone:** one-line header (Open · wordmark · Export). The stage is sticky with the photo at 40% of the screen height, or 68% with Bigger. Controls scroll underneath.
- **Desktop (≥900px):** 64px header, the stage fills the left side, and a 400px paper panel sits on the right.

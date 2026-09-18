---
sketch: 001
name: main-screen
question: "What layout structure best balances quick-request buttons, the smart keyboard, and one-tap PAIN/SPEAK for a bedridden, low-dexterity patient?"
winner: null
tags: [layout, main-screen, accessibility, aac]
---

# Sketch 001: Main Screen

## Design Question
CareTalk's main screen has to hold four things at once without ever hiding the two most urgent one-tap controls (PAIN, SPEAK): a bank of one-tap quick-request buttons, the smart predictive keyboard/suggestion chips, the message/output bar, and the language switch. Three structural approaches were built to see which balance feels right for a patient who may have limited or imprecise finger movement.

## How to View
```bash
open ".planning/sketches/001-main-screen/index.html"
```
Or open the published Artifact link.

**Sized for the real device.** The app is actually used on a fixed-mounted bedside touchscreen monitor, not a handheld tablet — so the frame defaults to the classic 17″ panel ratio (5:4, e.g. 1280×1024), with 13″ (4:3) and a modern wide (16:9) monitor as comparison presets in the sketch toolbar. Because it's fixed-mounted, one-handed reachability doesn't constrain the layout the way it would on a tablet — the extra space is used for bigger buttons and more visible at once, not padding. The screen itself uses CSS container queries (not viewport breakpoints) so button size, type scale, and grid density genuinely respond to whatever the frame's own width is, the same way the shipped app would respond to whatever monitor it's plugged into.

## Variants
- **A: Bar & Grid** — The quick-action grid (color-coded by category, Fitzgerald-key style) dominates the screen. Message bar with Undo/Clear/SPEAK sits fixed at top. The smart keyboard is tucked behind a "Type a message" bottom sheet so it never competes with the buttons for space.
- **B: Split Rail** — A persistent two-column layout for landscape tablets: quick-action grid on the left (~60%), the smart keyboard + suggestion chips always visible on the right (~38%), no tap needed to reveal typing. Message bar spans the bottom.
- **C: Message-First** — The message/output area and a large circular SPEAK button are the hero, with the keyboard/chips directly underneath as the primary interaction. Quick-action categories collapse into a horizontal color-coded tab rail (Things / Position & Rest / Comfort / Urgent) that expands one category's buttons at a time — trades one-glance button access for a calmer, typing-centric screen.

All three share: a persistent language toggle (EN/DE) that live-updates every label, chip, and quick-phrase; a full PAIN flow (location → severity 1–10 → optional type → generated sentence → auto-speak); and a SPEAK button that pulses and toasts the spoken sentence.

## What to Look For
- **Reachability under low dexterity**: in which variant do PAIN and SPEAK feel safest to hit without precision? Bigger targets, less clutter, no risk of mis-tapping a small keyboard key.
- **Grid vs. rail vs. tabs**: does having every quick-request visible at once (A/B) matter more than a calmer, typing-first screen with fewer visible buttons (C)?
- **Keyboard visibility**: is an always-visible keyboard panel (B) worth the screen space it costs, versus reveal-on-demand (A) or centered-and-primary (C)?
- **Category color coding**: does the Fitzgerald-key-style left-edge stripe (blue = things, green = position/rest, purple = comfort, orange = urgent) help scanning, or is it just noise at this button size?
- **Pain flow**: does the location → severity → type → review sequence feel fast enough for someone who is actually in pain right now?

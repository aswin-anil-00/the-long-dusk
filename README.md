# The Long Dusk

A calm, minimal countdown lock screen and desktop wallpaper built as a single, self-contained HTML file.

Instead of flashing red timers or stressful alerts, **The Long Dusk** translates remaining time into a quiet celestial arc: a soft sun slowly descends toward an OLED-dark horizon while the sky shifts smoothly from warm dawn cream and peach into deep indigo twilight.

## Features

- **Celestial Time Progression:** Computes the exact percentage of elapsed time between your start date and deadline to animate the sun's position along a dotted horizon arc and shift the ambient sky palette.
- **Poetic Phase Cues:** Updates a subtle phase line beneath the countdown (`Plenty of daylight` → `Golden hour` → `Dusk is near` → `Last light`), culminating in a starry *"Submitted. Well done."* night sky once the deadline passes.
- **Lock Screen & Desktop Safe Zones:**
  - **Portrait (Mobile):** Reserves the top 28% for system clocks/widgets and the bottom 12% for lock screen shortcuts, with 6% side margins.
  - **Landscape (Desktop):** Centers content within the middle 60% of the viewport so desktop icons remain unobstructed.
- **Hairline Milestone Tracker:** Automatically tracks milestones in `Asia/Kolkata` time—displaying completed items (dimmed), the next upcoming milestone with a live day countdown, and up to 3 detailed items with remaining steps compressed into minimal dots.
- **Zero Dependencies:** Pure HTML, CSS, and vanilla JavaScript in a single portable file with tabular serif numerals (`Cormorant Garamond`) and `prefers-reduced-motion` support.

## Quick Configuration

Open `index.html` in any text editor and edit the `CONFIG` block near the top of the `<script>` tag:

```javascript
const CONFIG = {
  eventName: "Submission Day",
  startDate: "2026-11-17T00:00:00+05:30",
  deadline: "2026-11-29T23:59:00+05:30",
  timeZone: "Asia/Kolkata",
  milestones: [
    { date: "2026-11-19", label: "Idea locked" },
    { date: "2026-11-22", label: "First draft" },
    { date: "2026-11-25", label: "Refine and test" },
    { date: "2026-11-27", label: "Final polish" },
    { date: "2026-11-29", label: "Submit" }
  ]
};
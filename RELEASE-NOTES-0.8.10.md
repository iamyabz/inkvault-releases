# InkVault 0.8.10

**Fixes the freeze after adding a sticky note or tape — and the three problems it was causing.**

Adding an object put the pen away, and putting the pen away made the app read every page you had drawn on, on the main thread. Six to seven seconds, every single time. That one line was behind three separate complaints:

- **The severe lag.**
- **Tape could not be moved at all** — dragging needs the pen out, so putting it away froze the thing you had just placed.
- **Sticky notes appearing in threes** — taps that queued during the freeze all arrived at once when it ended.

The pen stays out now, and reading your handwriting happens when you leave the reader.

**Sticky notes and tape stay on the page.** A card could be dragged off the paper, taking its header — the only part you can drag it by — with it, which left it unreachable and invisible.

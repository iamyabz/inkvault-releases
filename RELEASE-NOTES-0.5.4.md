# InkVault 0.5.4

**Two fixes for problems only a new user could hit.**

**Google retired the models InkVault was asking for.** If you set up a Gemini key recently, every page you tried to read came back with an error, because the model ids the app was sending are closed to keys created after Google's 2026 cutoff. Older keys kept working, which is exactly why this went unnoticed. InkVault now ships current models, and when Google retires one it reads the replacement out of Google's own reply, switches to it, and remembers — so the next time this happens the app fixes itself instead of waiting for an update. The error banner also stopped showing you raw JSON.

**Very long books no longer take the app down with them.** Importing a thousand-page book could run the device out of memory on the last step, losing every page it had just read. Rewriting a book of that size to embed a selectable text layer costs close to a gigabyte, and there is no cheaper way to do it on this platform. So InkVault now checks whether the device can afford that step before starting it. If it cannot, the book still imports completely — every page read, indexed, searched, and available to Ask AI. The one thing skipped is the invisible text layer inside the file itself, which only affects selecting text in other PDF apps, and the app tells you when that happens.

Imports also read fewer pages at once when memory is tight, not just when the device is warm.

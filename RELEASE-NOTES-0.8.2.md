# InkVault 0.8.2

**Tape and sticky notes actually appear now, and the ink is sharp again.**

The tape and stickies were being drawn — once, before the page had any size, so what got shown was an empty picture stretched to fit. They are drawn properly now.

The ink lost some of its crispness in the last release for a related reason: to make room for tape and stickies, every page's pen layer was put inside an extra container, and the pen renders slightly softer there. Pages without tape or stickies get the pen exactly as they did before, and only a page that actually has something on it uses the container.

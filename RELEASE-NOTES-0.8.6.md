# InkVault 0.8.6

**Fixes the crash, and sticky notes and tape now work the way they do in a notebook.**

**The crash.** Scrolling a long book could kill the app outright. Turning a page PDFKit had already released produced an arithmetic overflow, which in Swift is not a glitch but an immediate stop. It was introduced by the previous release.

**Tape has never actually been drawn** — in any version that offered it. The shared renderer only draws a strip once you peel it, because in a note the page image already carries it. A PDF carries nothing, so tape was saved correctly, placed correctly, and painted as nothing at all.

**Sticky notes are real notes now.** Write inside a card with the same pen you use on the page, drag it by its header, pull its corner to resize, hold it for colours, put it away as a tab in the margin. None of it needs the pen switched off any more — an object takes the touches meant for it and the pen keeps the rest.

**Tape can be drawn.** Pick "Draw a tape shape" and drag out a strip exactly over what it should cover, instead of getting one in the middle of the page.

**Ink no longer blinks when you zoom.** It also no longer redraws every page you have visited each time the zoom changes, which is what could exhaust memory on a big book.

**Exports keep your tape and cards.** A flattened copy carried the ink and nothing else.

**And the app now records its own crashes**, so the next diagnostic report says what happened instead of guessing.

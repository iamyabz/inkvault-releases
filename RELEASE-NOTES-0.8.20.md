# InkVault 0.8.20

**Sharper ink at normal reading zoom, and marks appear on Mac without reopening the book.**

**The ink was being drawn at too few pixels at exactly the zoom you read at.** A page filling an iPad screen is shown about half again as large as its own size, and the app was rounding that down to "no magnification" — so it drew the ink small and stretched it. It now always draws at least as many pixels as the page is being shown at.

**Annotations arriving from another device now appear in a window you already have open.** The marks were reaching the Mac correctly; the reader only looked for them at the moment a document was opened, so if they landed a minute later you saw nothing until you closed and reopened it.

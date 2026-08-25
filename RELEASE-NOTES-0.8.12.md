# InkVault 0.8.12

**Three slow things taken off the path you wait on.**

**Closing a marked-up book froze the app for seven seconds.** Reading your handwriting rebuilt the whole keyword index — 88 MB on a big library — on the main thread. It now happens in the background.

**Writing your notes down was doing it a page at a time.** Each page saved the entire library; ten annotated pages meant ten full saves before anything appeared. Now it is one.

**On Mac, opening a document read the whole document first.** Every page was lowercased for ⌘F between the click and the window, which on a 900-page book is several seconds with nothing on screen — hard to tell from a click that did nothing. It happens in the background now, and ⌘F also finds what you wrote on a page, not just what the page says.

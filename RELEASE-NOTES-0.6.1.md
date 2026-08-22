# InkVault 0.6.1

**Fixes for everything 0.6.0 got wrong.**

**The page grid could freeze or crash the app.** Scrolling quickly through a long book started far more page renders than it could handle, all competing for the same file. It now renders one page at a time and stops work for pages you have scrolled past. This was the cause of the freeze when selecting text after using the grid.

**The Ask AI window lagged behind your finger and shook while moving.** Two separate mistakes, both fixed: it now tracks your finger exactly and moves without redrawing the conversation on every frame. The resize handle has also moved off the send button.

**Tapping a page now re-points an open Ask AI window at it**, instead of quietly staying on the page you came from. Scrolling does the same.

**The page slider is smooth.** It was quantising over sixteen hundred steps.

**The page grid and contents list have been rebuilt.** The grid opens at the page you are on and marks it, sizes itself to the screen, and shows page numbers. Contents shows where you currently are, indents properly, and switches between chapters and the full outline.

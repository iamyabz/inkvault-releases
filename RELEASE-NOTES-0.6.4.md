# InkVault 0.6.4

**The long freeze is fixed, and it was Select All.**

Selecting all of a very long book made InkVault read and hold every page at once — twenty-six seconds frozen and nearly two gigabytes on a 1633-page textbook. On a book, Select All now selects the page you are on, which is what anyone actually wants; nobody needs sixteen hundred pages on their clipboard. Dragging a selection past the end of a page is capped for the same reason.

**Markup with a finger now works.** It never did: InkVault was asking the system for pencil-only drawing, so anyone without an Apple Pencil could turn markup on, draw, and get nothing — with the pen lit and the toolbar showing. Pencil users were unaffected, which is why it went unnoticed.

**Markup also stopped leaving empty files behind** for every page you scrolled past — there were over nine hundred of them — and no longer keeps a drawing surface in memory for every page of a long book.

**You can see what you're typing in Ask AI.** Lifting the window above the keyboard wasn't enough when the window was taller than the space left; it now resizes to fit.

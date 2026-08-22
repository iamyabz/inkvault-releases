# InkVault 0.6.6

**Scrolling a long book, then selecting text, no longer stalls the app.**

This is the third attempt at this one, and the first two were wrong about the cause. Selecting all of a book was a real problem and is fixed, but it was not what you were hitting.

InkVault was creating a full drawing surface for every page you scrolled past — even if you never turned markup on. Reading a sixteen-hundred-page book that way built up more than a gigabyte while you scrolled, and the app was still busy with it when you went to select text. That is why selecting always seemed to be the trigger: it was simply the next thing to ask for attention.

A drawing surface is now created only when markup is switched on, or when a page already has marks to show. Reading costs nothing.

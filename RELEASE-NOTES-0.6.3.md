# InkVault 0.6.3

**You can see what you're typing.** The Ask AI window now lifts above the keyboard while you type and drops back when you're done, without losing the place you put it.

**Contents finds more of your book.** Some PDFs carry only a token contents — cover, contents, index — while the book itself has forty chapters. InkVault was trusting that token list over the chapter headings it had already read. It now uses whichever actually describes the book.

**Diagrams look like diagrams.** Softer boxes, proper arrowheads, more room to breathe.

**Groundwork for a freeze some long books hit.** A single action deep in a large book can stall the app for several seconds and take a large amount of memory that isn't given back. The cause isn't identified yet, and rather than guess, this build records exactly what each action in the reader costs. If you hit it again, sending the diagnostics report from Settings will point straight at it.

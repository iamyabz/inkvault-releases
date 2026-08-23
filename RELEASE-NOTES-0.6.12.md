# InkVault 0.6.12

**The freeze is iOS analysing pages it has no reason to analyse.**

The diagnostic now names the file and rules out InkVault's own text recognition entirely. Checking every one of that book's 1394 pages, all of them already carry searchable text — so the system is running its own image analysis over pages that need none, and doing it on the thread that draws the screen.

This build switches that analysis off through the proper API, and where it cannot be recognised, records exactly what is attached so the next report says rather than leaves it to guesswork.

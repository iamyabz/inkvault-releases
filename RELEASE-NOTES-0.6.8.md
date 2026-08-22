# InkVault 0.6.8

**Closing in on the stall in long books.**

The last build's diagnostics finally recorded what happens during the freeze instead of skipping it: memory climbs steadily for about fifteen seconds and then levels off while the app is still busy. That rules out most of what it could have been, and it rules out the fixes already tried.

This build adds the last piece — while the app is unresponsive it now records what it is actually doing, once a second, from outside. One more report and this stops being guesswork.

**A real fix in the meantime:** InkVault was still creating a drawing surface for pages that had no marks on them. Older versions left behind an empty file for every page you scrolled past, and those empty files were being mistaken for real marks. They are now recognised and cleared away as each book is opened.

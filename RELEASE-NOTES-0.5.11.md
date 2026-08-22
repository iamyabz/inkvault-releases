# InkVault 0.5.11

**A real 1633-page book showed the last fix wasn't enough.**

0.5.4 added a check that stops a very long import from running the device out of memory. It worked out how much a book would cost from a measurement taken on a Mac. The first real book to test it — a 1633-page surgery textbook on an iPad — cost more than twice that, peaking at 2.8 GB. It finished, because the check leaves a wide margin, but only just, and the same import on an iPhone would not have.

The estimate is now based on what a device actually does, not what a Mac does. More importantly, InkVault no longer relies on the estimate being right: while it works, it watches how much memory is genuinely left, and if it starts running out it stops that step cleanly. Your document is untouched when that happens — it is already fully imported, indexed and searchable — and the app tells you plainly what was skipped.

**Progress reporting is quieter too.** That book wrote 544 near-identical progress lines into the diagnostics report, burying everything useful around them.

# InkVault 0.6.10

**Correcting the tool, not guessing again.**

The last release turned off a system feature that looked like the cause of the freeze in long books. It was not, and checking why turned up a fault in the diagnostic itself: it could have been watching the wrong thread the whole time, which would make its answer meaningless.

That is fixed, and the diagnostic now also records whether the app is actively working or merely waiting on something else — the single fact that separates "this is ours to fix" from "this is us waiting". It was never being recorded, and it decides everything.

No behavioural change in this release. The last one shipped on a reading that could not be justified, and it did not work.

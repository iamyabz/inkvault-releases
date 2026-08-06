# InkVault 0.3.2

## A crash when opening a video

If the main window was at or near its narrowest, opening a video could quit
InkVault outright.

All three columns (sidebar, document, inspector) have to fit across the window.
When they cannot, macOS raises a layout error and the app is terminated rather
than simply looking cramped. InkVault has enforced a minimum window width for
this reason for several releases, but that minimum was set at the width where
the problem stopped reproducing, not at a width proven to be safe. A window
sitting exactly on the old limit still had only 50 points of room to spare, and
that was not enough.

The floor is now 1180 points, which leaves 150 points of headroom instead of 50.
If your window was narrower than that it will be widened once on first launch.
Nothing else about your layout changes.

## Crash reports that explain themselves

macOS writes an excellent crash report, but it does not record the error
message, only where the failure happened. That is why this crash could be
pinpointed to the exact line of Apple's layout code and still not be explained.

InkVault now captures the real error message as it exits and sends it with the
next report. This is a diagnosis change, not a workaround: if the underlying
layout fault recurs, the report will name the exact constraint, and the window
minimum can come back down instead of being raised again.

---

**Requires** macOS 14 or later on Apple Silicon.
Questions: support@getinkvault.com

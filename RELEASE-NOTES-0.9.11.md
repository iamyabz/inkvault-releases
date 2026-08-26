# 0.9.11

## Opening a book stops going to iCloud every time

When another device has annotations this one has not got yet, the reader goes
and fetches them. If those annotations genuinely are not on the server — a
device that announced them and never finished uploading — that check never
stopped being true, so opening that book was a network round trip every single
time, for ever. It now gives up after a few tries and starts again the moment
anything arrives.

## Better diagnostics for annotations that will not arrive

When a fetch fails it now records which device's annotations were being asked
for and under which version, so a diagnostic report can say what went wrong
rather than only that something did.

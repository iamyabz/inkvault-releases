# 0.9.6

## Deleting something deletes it everywhere

Deleting was a local act. Other devices only found out from a sweep on the NEXT
sync — and that sweep compares this device's record of what IT has published
against what it still holds. Two consequences, both of which read as "I deleted
it and it is still on my iPad":

Nothing was said at the moment of deletion, so until the next sync ran, no other
device had been told anything.

And a document this device never published was not in that record at all, so
deleting something that arrived from another device published no tombstone on
any pass, ever.

Deletions are now published where they happen, on both platforms, when a
document goes to Recently Deleted and again when it is destroyed for good. The
old sweep stays as the backstop for a deletion made while offline.

## Import straight from Photos

Photos and videos can be imported from the photo library. Photos become one
proper multi-page PDF in the order you picked them, and go through the same
pipeline as any other PDF. Videos stay videos and are transcribed as usual. A
short screen before importing lets you reorder, remove, rotate and name.

## Selecting handwriting lands on the handwriting

Copying from a handwritten page put the selection nowhere near the ink. The
reader that reads handwriting returns no positions, so the invisible text was
laid out by formula. It is now placed using line positions found on the device,
paired with the words — and only where the two agree about how many lines there
are, so it never confidently puts text on the wrong line.

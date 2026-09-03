# 0.9.44

Mostly repairs, and several of them are the kind that only show themselves
when something has already gone wrong.

## Your handwriting stays put

The most important fix in this release is one you would never have seen until
the day it mattered. When the iPad could not write a page of ink to disk —
a full disk, or any other I/O failure — the app went on believing it had
saved. It then dropped its only remaining copy from memory, and the note
reopened showing the version from before your session, with the shelf having
said "Saving…" the whole time.

That was true for notes on the infinite canvas, which is what a new note uses.
A failed write is now remembered as failed: the ink stays in memory, the next
save tries again, and the notes list says **Couldn't save** instead of quietly
claiming otherwise.

## Marking up a document

Three separate faults could leave the pen inert on a PDF or a photo while the
toolbar answered normally — colours and pens selectable, nothing written. None
of them were in the note engines, which is why handwriting worked on the same
device at the same moment.

The reader applied a tool change one selection late, so picking up the pen gave
the page whatever you had been holding before. Anyone arriving from a note with
Move Objects or the lasso still chosen got an ink-selection tool on the page,
which never marks, and no amount of tapping pens or colours corrected it. A
canvas built once and re-attached later came back holding its old tool. And a
one-page document — which is what an imported photo always is — could end up
with no canvas at all, because the machinery that hands one out relies on pages
scrolling into view, and a single page never scrolls.

**Move Objects no longer leaves the page in selection mode.** It has no meaning
on a document, so it now stands the canvas down and lets you move tape and
cards, which is what it is for.

## Undo

Several things were not undoable at all, and the Undo button stayed lit anyway
— so pressing it took back the last thing you *wrote* instead.

- **Moving, resizing, rotating, recolouring or peeling** an object registered
  nothing. Because reaching any of those means switching tool first, it looked
  like a bug in the tools: write a sentence, change tool, nudge a photo, press
  Undo, and the sentence went.
- **Tape and cards on a document** were the same, and are now undoable too.
- **Ink written on a sticky note** never reached the undo stack, so Undo took a
  stroke off the page underneath instead.
- **Draw-and-hold shapes** replaced the stroke you had just drawn without
  recording it, so Undo left the shape and removed something older.
- **Adding a page** threw the whole history away. It no longer does; removing
  or reordering pages still has to.
- The paged view reassigned the pen on every screen update, which cancels a
  stroke in progress — so sometimes there was no "last one" left to undo.
- **Undo and Redo now dim when there is nothing to take back**, so a spent
  history is no longer indistinguishable from a button that did nothing.

Undo is better than it was and is not yet what it should be. Moving selected
ink still clears the history, for a reason that needs a deeper change than this
release makes.

## Highlighter

**Scribbling over something with the highlighter no longer erases it.**
Scratch-to-erase is for ink; a highlighter that deleted what you highlighted
was catching people out. This fix was written some time ago and, through an
oversight, never actually reached a build until now.

The Marker pen now uses its own ink. One visible consequence: it draws a little
more evenly than before. One invisible one, which was a real fault: the Marker
pen had been blending like a highlighter in **exported** PDFs, and no longer
does.

The highlighter still covers what is under it rather than sitting behind it.
That is understood in detail now — it needs its own rendering layer, and the
first attempt cost more than it bought.

## Drawing with a finger

**"Draw with a finger" now works for handwritten notes.** It only ever reached
document markup: both note engines asked the system for its default, and that
default means *pencil only* unless a system tool palette is on screen, which
this app does not use. Anybody without an Apple Pencil could turn the setting on,
watch it work on a document, and still be unable to write a note.

## Two-page view, tape, and find

- Switching out of the two-page book view read each page from disk as it
  rebuilt, which could happen before the last half-second of ink had been
  written. Those strokes were then overwritten. Both views now commit what they
  are holding before the other one reads anything.
- A strip of tape sat above the page and took the pen's touches instead of the
  canvas — worst on a peeled strip, which is nearly invisible, so the pen simply
  looked dead over part of the page.
- Searching an infinite canvas read it in tiles, and a word sitting on the seam
  between two tiles was cut in half, read as neither, and remembered as absent.
  The tiles now overlap.

## Deleting a note deletes it everywhere

A deleted note left its entry in the library behind: it stayed in All Files,
stayed in search results, and its Edit button opened a blank editor for a note
that no longer existed — while the dialog promised search entries were removed
too. The library entry now follows the note into Recently Deleted, back out
again on restore, and away for good on delete.

## Imports that cannot be read no longer leave litter

If every page of something failed to read, the import stopped — but the copy it
had already made stayed on disk, invisible to the app and impossible to remove
from inside it, while counting against your storage. That copy is now cleaned
up, and only ever when nothing else refers to it.

## Diagnostics

A diagnostic report now records which kinds of touch are allowed to draw, and
says when a page is first given something to draw on. A report could previously
show markup being set up and nothing being saved and give no way to tell "the
canvas refused the input" from "there was no canvas" — which is exactly the
ambiguity that made one recent problem hard to place.

## Also

Sticky notes are indexed: what you type on one is now searchable and available
to Ask AI, like anything else on the page. Study history on iPad matches the
Mac. Several smaller repairs to two-page inserts, page deletion, and writes that
could race each other.

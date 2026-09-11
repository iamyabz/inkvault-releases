# 0.9.50

This version gathers up everything since 0.9.44, including five versions that
were never published. Five changes matter more than the rest.

On iPhone and iPad, choosing Apple's speech engine sent your recording to
Google. It no longer does. A library file that could not be read was treated
as an empty library, which could be saved over the real one and send your
documents to Recently Deleted on your other devices. It is now set aside and
never written over. Emptying Recently Deleted could delete a file that a
document still in your library was using; any file still in use is now kept. A
heavily annotated book could outgrow what InkVault would send, and handwriting
past that point never reached your other devices. That limit is gone. And the
privacy policy has been corrected to say exactly what leaves your device, so
InkVault asks you to accept the updated terms once.

You can also now share any document as a PDF, with or without your markup.

## Apple's speech engine no longer sends your recording to Google (iPhone and iPad)

On iOS 26 and later, the record and import screens offer Apple's own speech
engine, described as working entirely on the device. From the day that option
appeared, the app sent the recording to Google's Gemini instead, and with no
Gemini key set it sent it anyway, to be refused. Choosing Apple's engine no
longer sends your recording anywhere to be transcribed, and if the engine you
chose cannot run, the import stops and says why rather than using another.

The caption beside that choice now says plainly where your audio goes: it
isn't sent anywhere to be transcribed. With a Gemini key set, the transcript's
text is still sent to Google to make it searchable, and for a video, to name
its chapters.

## A damaged file can no longer empty your library

If your library's file could not be read, after a disk error or an interrupted
copy, InkVault loaded an empty library, saved that over the real file, and
could send every document to Recently Deleted on your other devices. Now it
keeps a copy of the unreadable file where it can, refuses to save over it, and
pauses sync until it can be read; changes made meanwhile are not saved.
Pending changes are also now saved when the Mac quits or an iPhone or iPad
goes to the background.

## Emptying Recently Deleted keeps files your library still uses

Emptying Recently Deleted, or a document leaving it by itself after 30 days,
deleted the files those trashed documents named. If a document still in your
library used the same file — the same file imported twice, or restored under
another name — that file went too. A file any document still uses is now kept,
recognised both by name and as the same file on disk, and a library that could
not be read in full deletes nothing at all.

## Handwriting reaches your other devices

A document's annotations had a size limit that a heavily annotated textbook
could reach at around eighty pages. Past it, whole pages of handwriting were
quietly left out of what went to your other devices. Annotations now travel in
pieces, with no overall limit; in testing, a book with 369 annotated pages
arrived on a Mac in full. While newer annotations are still arriving, the Mac
keeps showing the last complete set and says so in its toolbar. A device on an
older version shows fewer annotated pages until it updates.

The iPad's highlighter now lets the words show through on the Mac and in
exported PDFs. And on the Mac, markup made on a differently sized copy of a
page can no longer hide other devices' markup on that page.

## Sticky notes keep what you type (iPhone and iPad)

Words typed on a sticky note inside a handwritten note were never saved: the
card forgot them when it closed, and reached the Mac empty. That is fixed;
anything typed before this version was never stored and cannot be brought
back. In a note, a finger now peels tape even while a pen is selected.

## Privacy policy and terms

The privacy policy, and what the app says about privacy, have been corrected
to describe exactly what leaves your device and when. InkVault asks you to
accept the updated terms once, when you first open this version.

A file opened before you accept now waits, and is imported afterwards. On the
Mac, crash reports and building search data with your Gemini key wait for
acceptance too; on iPhone and iPad, so do sync and search indexing.

InkVault now takes any API key out of an error message before it stores, syncs
or logs it. Before this version, a failed request to Google could leave your
Google key in that message, and on a Mac with sync on it could reach a record
in your own iCloud, which Apple can read, and stay there. If that may apply to
you, you can replace your key in Google AI Studio.

## Share a PDF, with or without your markup

The reader's Share menu, on iPad, iPhone and Mac, offers **Without Markup**;
**With Your Markup**, every page with every device's ink, tape, cards,
pictures and text boxes; and **Only Marked Pages**, the marked pages and
inserted blank pages, each with a footer naming the page. The file is deleted
when the share sheet closes. If a device's markup does not fit a page, it is
left off, the page is named, and you can share anyway.

The export this replaces, on iPhone and iPad, could put handwriting on the
wrong page when blank pages had been inserted, and could quietly send the file
without your markup.

## Marking up a PDF (iPhone and iPad)

Marking up now happens on a new canvas, built like the note editor's: ink is
redrawn at the zoom you are at, and the page at the screen's full resolution,
so both stay sharp. Found before release and fixed: moving far through a long
book, or inserting a blank page partway in, could delete ink on other pages.

What a note could do, a PDF now can:

- **Shapes and erasing:** Hold to shape, Scribble to erase (never with the
  highlighter), dashed and dotted lines, tape from a drawn shape, and the
  Pencil's double-tap for the eraser.
- **On the page:** text boxes; pictures under your ink that turn with two
  fingers, even one copied on your Mac; sticky notes at your finger, in the
  colour you pick; and Put Annotations Away for every card at once.
- **Selecting:** the lasso or a long press on ink, then Cut, Copy, Duplicate,
  Delete and Paste, or ⌘X, ⌘C, ⌘D, Delete and ⌘V. ⌘Z and ⇧⌘Z undo and redo.
- **Undo** covers text boxes, pictures, sticky notes and selected ink, on any
  page.
- **Fit Width** returns to the fitted page on the same line; **Select text**
  copies words without putting the pen away.
- Another device's ink can be rubbed out, and the Mac's tape peeled.
- **Delete Page** asks first if the page has writing on it, both for an
  inserted page in a PDF and in a note.
- Text boxes are **searchable** after you close the reader, with no API key,
  and Ask AI no longer calls their words your handwriting.
- A hand resting on the page no longer brings up a card's or picture's menu.

Closing a heavily annotated book could hold up the iPad while it prepared your
annotations for other devices. That now runs in the background, once when you
leave the book or the app, redrawing only changed pages.

## Summaries

- **Brief, Standard or Thorough**, set in Settings on each device, and
  Regenerate can use another length once.
- **Your own instructions**, up to 600 characters, added after InkVault's own
  rules and framed so they cannot override them.
- **Tables** are drawn as tables on the Mac, the iPad and in exported PDFs.
- **The AI provider you chose writes the summary, or nothing does.** No Gemini
  key is needed for it; if it has no key, you are told which to add, and a
  summary is never quietly written by Gemini instead. Search, reading
  handwriting and indexing still use Gemini.
- **A failed Regenerate never replaces your summary.** On the Mac, a failure
  used to replace it with an apology, which then synced.
- On iPhone and iPad, closing the summary sheet no longer loses an edit.

## Quizzes

After a quiz, each question has **Ask about this**: a conversation about that
question that knows the answer, your choice, what you crossed out and what you
highlighted, and cites your source. It opens beside the paper on the Mac and
as a sheet on iPad and iPhone.

Highlight a question's words by dragging on the Mac, or on iPad and iPhone
with the Pencil or, once the new highlighter button is on, a finger.
Highlights and conversations aren't sent to your other devices, and
highlights are saved once you finish the quiz.

A quiz on chosen pages is now written from those pages, not the whole book;
front matter no longer yields chapter and ISBN questions; and a whole-document
quiz no longer freezes the app.

## Importing (iPhone and iPad)

- **Stop says what it keeps.** It promised that pages already read were kept,
  which was never true: a document is only added once complete. Files already
  imported stay; the one being read is not added, even if it finishes after
  you press Stop.
- A file that failed to copy in, or a pasted link that was not a YouTube link,
  could make InkVault read the same file twice, and pay twice.
- A YouTube link pasted during another import waits its turn.
- A stopped or failed import leaves nothing behind in your library: a file
  is prepared on the side and added only once it is complete.
- **Whisper before its model arrives.** Choosing Whisper with no model
  downloaded used to accept the recording and then fail, taking it out of the
  queue. It now waits there until you download a model in Settings, and the
  record screen won't transcribe until one is ready.
- Importing a spreadsheet again replaces the copy you have. One imported
  before this version is added beside the old copy instead, because its
  original name was never kept.
- On iPhone, an import shows progress on the Lock Screen and in the Dynamic
  Island. The Lock Screen never shows the document's name.
- A Home Screen widget offers Import, Record and Search.

## Mac

- **Video full screen** is now the window's own, so the player no longer gets
  stuck afterwards. Leave it with ⌃⌘F or the button, not Escape. The speed
  menu matches the picker, a speed survives a pause, and the arrow keys skip
  ten seconds.
- A recording's AI can now answer beyond the recording, and says when it does.
- Export Backup and Restore Backup run in the background, can be stopped, and
  say plainly when they fail. Stop also ends a local Whisper transcription,
  which on a long lecture could stall its import.
- Dropping a folder no longer makes the app almost unusable, and files dropped
  inside a folder go into it.

## Also

- **Spotlight** (Mac, iPhone and iPad) can find documents by name if you turn
  it on in Settings. It indexes names, never contents.
- **Notes (iPad):** the infinite canvas no longer stops at an edge above and
  left of where you first wrote.
- **Inserted pages:** a new blank page is blank and keeps what you write on
  it; search results and jumps land on the right page; a page keeps one name,
  such as 412a, after reordering.
- **Your API bill (iPhone and iPad):** typed sticky notes on a PDF were re-read
  by Gemini at every launch. Now only a changed one is.
- **iPhone and iPad:** books open on the page; very long books open without
  freezing; the library list fills as soon as it loads.
- Searching while sync removed a document could crash the app.
- Less work in the background: annotating no longer rewrites your whole
  library file, and a device receiving your annotations no longer sends the
  document back. The library also uses less memory.

# 0.9.0

## Blank pages you can slip between two pages of a PDF

Insert your own blank paper anywhere in a document and write on it, on the Mac
and on iPhone/iPad. In full screen, the tape and sticky menu now offers **Blank
page after this one**; while you are on one it offers to remove it.

The book's own numbers do not move. A sheet after page 412 is **412a**, and 413
is still 413. Ink, search, citations and sync are all filed by page number, so
renumbering the book would quietly re-point every one of them.

Handwriting on a sheet is read and searchable like any other annotation, answers
name it as your own paper rather than the book's, and asking about a sheet also
sends the page it sits beside.

## Annotations now sync both ways

Marks made on the iPad and on the iPhone are combined instead of one device
ignoring the other. Write on page 42 on one and page 42 on the other and both
sets of handwriting appear on both, and on the Mac. Blank sheets travel too, and
deleting one on either device removes it on the other.

Each device now publishes its own copy rather than every device writing over the
same one, so no device can overwrite another's work.

**You can add to what another device wrote, but you cannot rub it out from a
device that did not write it.** Erasing across devices needs per-stroke identity
that PencilKit does not provide, and the alternative loses handwriting.

## Fixed

- **Opening an annotated book on a second iOS device erased its annotations
  everywhere.** That device could not download the sidecar, found nothing of its
  own, and cleared the document's published annotations — so the Mac stopped
  showing marks that were still on the iPad.
- Annotations on a long book were drawn on the wrong page after the first
  inserted sheet, and on windowed books generally.
- A page with nothing printed on it but your own handwriting can now be asked
  about.

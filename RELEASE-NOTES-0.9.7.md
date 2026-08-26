# 0.9.7

## Books keep their table of contents

Making a document searchable rebuilt the whole file, and the rebuild could not
carry an outline — so every book imported into InkVault lost the contents its
publisher put in it. A 402-page orthopaedics text has 45 chapter entries; the
copy the app read had none. That is also why a 1,394-page textbook had to
recover its chapters from the titles printed at the top of each page.

A document that already carries proper text needs nothing added to it, and is
now left exactly as it is. Its outline, links and annotations survive, and so do
its original bytes.

## Scans stop getting bigger and blurrier

The same rebuild decoded and re-encoded every image on the way through. A 150
dpi scan went in at 31.4 KB a page and came out at 34.4 KB — the same pixels,
one generation of JPEG quality poorer, with a colour profile nobody asked for,
in a file 19% larger. It then replaced the original, so none of it could be
undone.

Scans that already carry recognised text are now left alone too. A page that
genuinely has no text still gets one, which is what the rebuild was always for.

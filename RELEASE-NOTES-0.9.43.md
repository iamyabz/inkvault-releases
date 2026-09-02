# 0.9.43

## Sharing no longer leaves a copy behind

Choosing Share has to build the file before the system share sheet can offer it,
and backing out of that sheet used to leave it on disk — a 300 MB textbook, in
one real case. It is cleared now: when the app starts, before every share, and
shortly after you come back to the app.

Cancelling at the earlier steps never wrote anything and still doesn't, and
nothing is ever written outside InkVault's own temporary space. Importing a
shared file also tidies up its own scratch copies when something goes wrong
partway.

## Importing a shared file says what it is doing

Opening a `.inkvault` looked like nothing had happened until the documents
appeared some seconds later. It now says it is reading the file, and then that
it is importing — which matters most for a shared folder, where the second half
is copying gigabytes.

## iPhone and iPad

The opening animation could keep playing and never hand over to your library,
leaving the app unreachable until you switched away and came back. It now always
ends: it waits for your library, and gives up waiting after about six seconds
either way. The ink drop also falls a little more slowly.

**iPhone no longer offers to start a handwritten note.** There is no pencil
there, so it opened a page you could not usefully write on. Reading notes made
on your iPad or Mac is unchanged, and so is everything else the phone is good
at — recording audio, the scanner, photos, importing files.

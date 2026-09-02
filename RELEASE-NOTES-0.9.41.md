# 0.9.41

## The opening animation could get stuck

On iPhone and iPad the animation could keep playing and never hand over to your
library, leaving the app unreachable until you switched away and came back. It
now always ends: it waits for your library, and gives up waiting after about six
seconds either way. The ink drop also falls a little more slowly, so there is
something to watch rather than something that is over before you have looked.

## Mac

No changes. 0.9.40's drag-into-folder fix and the share sheet are unchanged.

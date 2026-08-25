# InkVault 0.8.21

**New marks now reach your other devices — previously they were always one session behind.**

Marks you made were being checked for changes by looking at the files on disk, but those files are written in the background a moment after you close the reader. So the check ran too early, saw the state from before your last strokes, decided nothing had changed, and sent nothing.

The next time you closed the reader it would send the *previous* session's work — which is why the Mac kept showing older markings and never the newest ones.

The check now looks at the marks themselves rather than at the files, so it cannot be fooled by timing.

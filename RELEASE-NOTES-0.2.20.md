## InkVault 0.2.20

### iPhone/iPad: the file pickers actually open
"Choose Files", "Choose a Recording" and "Choose a Video" could do nothing at all — no picker, no error, nothing. SwiftUI's file importer refuses to present from inside a sheet that shares a screen with other sheets, which is exactly where the import screen lives.

The picker is now opened directly, so the button press *is* the presentation and there's nothing left to lose a race against.

### iPhone/iPad: Settings changes show immediately
Choosing a different answer model appeared to do nothing until you left Settings and came back. The choice was saved instantly — the screen simply wasn't told to redraw. Every screen now sees settings changes as they happen.

### Errors say what went wrong (0.2.19)
"The operation couldn't be completed. (…GeminiError error 1.)" was the app showing you an internal case number. Every error now reads as a sentence naming the cause and what to do — a rejected API key, exhausted quota, a page blocked by Google's safety filter, a service having a bad day.

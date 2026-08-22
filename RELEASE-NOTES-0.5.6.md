# InkVault 0.5.6

**Handwritten notes, specifically.**

The last two releases fixed the model errors that stopped new API keys from reading anything. Reading a handwritten note takes a slightly different path through the app, and that path was still skipping part of the fix: it worked, but paid a failed request on every single page before recovering. On a notebook that is invisible. On a long import it is thousands of wasted calls.

**And a quieter one.** InkVault asked every model for maximum consistency, which was right for the previous generation and is not right for this one. Google's guidance is that the new models can start looping when pushed that way, and a looping model on a page read runs until it times out and reports the page as failed. That setting is gone for the current models and kept for the older ones, where it was measured and correct.

Audio transcription was the one request in the app that built its settings by hand, so it had been missing both the speed setting and this fix. It now goes through the same path as everything else.

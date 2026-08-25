# InkVault 0.8.14

**Fixes documents that could neither be opened nor synced, despite being right there on the device.**

An app's storage folder on iPhone and iPad has an identifier in its path that **changes** when the app is reinstalled or restored from a backup. The library remembered the old address, so files that were still on the device looked missing — the reader said "the file hasn't reached iCloud yet", and sync quietly skipped them, because it only uploads documents whose files it can find.

On one iPhone that meant **58 of 69 documents had never been uploaded**, with no error shown anywhere. Addresses are now corrected automatically when the app opens, and those documents will publish on the next sync.

**Asking about a page no longer asks about page 1.** Opening a book straight to page 500 and tapping Ask sent the question about the first page instead. Scrolling a single page used to work around it.

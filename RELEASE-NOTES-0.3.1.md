# InkVault 0.3.1

A correctness fix to the terms screen introduced in 0.3.0.

## The acceptance screen now actually holds the app back

In 0.3.0 the screen blocked the window, and only the window. Behind it, InkVault
was already contacting the licence server and starting your trial, importing
from any watched folder, and syncing. Someone who opened the app, read the
terms and decided to quit had already had work done on their behalf.

Nothing starts now until you press Continue. The same fix applies on iPhone and
iPad, where imports and crash reporting were also running behind the screen.

Nothing else changed. Your library, your licence and your settings are untouched,
and if you already accepted the terms in 0.3.0 you will not be asked again.

---

**Requires** macOS 14 or later on Apple Silicon.
Questions: support@getinkvault.com

# InkVault 0.5.8

**Checking the parts the last release did not check.**

0.5.7 tested reading a page against a real API key and reported it working. It had tested a different function from the one handwritten notes actually use. The real one is now tested — as it is normally sent, in the fallback mode it retries with, on the stronger model it escalates to, and starting from the outdated model setting that existing installs are actually carrying. All four read the page correctly.

**Search was never tested at all.** The part that turns your notes into something searchable had not been checked against a new key once. If it had been broken, InkVault would have looked like it was working and simply found nothing. It works.

**Recordings could still get stuck.** Audio transcription was the one request in the app that did not share the recovery path, so it could ride out a retired model only if something else had hit it first. It now recovers on its own like everything else.

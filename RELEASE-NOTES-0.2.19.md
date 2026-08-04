## InkVault 0.2.19

### Errors say what went wrong
"The operation couldn't be completed. (InkVaultCore.GeminiEngine.GeminiError error 1.)" was the app showing you an internal case number instead of an explanation.

Every error you can be shown now reads as a sentence that names the cause and what to do about it. An API key that was rejected, quota that ran out, a page Google's safety filter blocked, a service having a bad day. Where Google explains itself, its own sentence is passed through rather than buried in raw JSON.

That last one mattered more than it sounds: a page blocked by the safety filter and a page too large for one response used to be the same silent "no text". They want opposite responses from you, so they now say different things.

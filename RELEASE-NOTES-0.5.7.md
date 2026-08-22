# InkVault 0.5.7

**Tested against a real new API key, which found two more problems.**

InkVault can recover on its own when Google retires a model: it reads the replacement out of Google's reply and switches to it. Tested properly for the first time, that recovery turned out to fail — for exactly the people it was written for. It switched to the right model and then sent it a setting only the old one understood, so the request failed anyway. Both halves are fixed, and the recovery is now verified working end to end.

**Speed, confirmed rather than hoped.** Measured on a new key: answers come back in about 0.7 seconds and a page reads in about 0.8, which is the same speed as before the model change. That only holds because InkVault tells the fast model not to deliberate; left alone it takes roughly twice as long. The model picker in Settings now shows real measured timings instead of estimates.

Follow-up questions in a conversation were an open question on the new models. They work.

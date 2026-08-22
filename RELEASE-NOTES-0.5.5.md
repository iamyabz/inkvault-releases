# InkVault 0.5.5

**Speed, after the model change.**

0.5.4 moved InkVault onto Google's current models, because the previous ones had been closed to newly created API keys. What it did not do was tell the new models to hurry. Gemini's newer generation reasons at length by default, which is right for a hard question and wrong for reading a page or answering from notes InkVault has already pulled up — so imports and answers would have been slower than before, for no benefit.

The fast models are now asked for the fastest setting, and the deep model is left to think, which is what you picked it for. If a future model ever refuses that instruction, InkVault asks again without it rather than failing the page.

**One quiet risk closed.** InkVault can follow Google's own instructions when a model is retired. That must never apply to the model that builds your search index — swapping it would leave old and new entries in your library that cannot be compared, and search would gradually stop making sense with nothing to show you why. It is now excluded outright.

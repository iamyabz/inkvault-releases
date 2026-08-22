# InkVault 0.5.9

**You can now tell which parts of an answer came from your notes.**

Ask AI could answer a question that your notes did not cover, in a reply that looked exactly like one drawn from them. That was most visible when a note had failed to index: the note was empty, InkVault asked about it anyway, and the answer came entirely from the model's general knowledge with nothing to say so.

Two changes. **A document that hasn't been read yet is no longer treated as evidence** — InkVault says so and tells you to check your API key, instead of quietly asking a question about a blank page. If you have several documents selected and only some are still indexing, it still answers, and says which ones it hasn't seen.

**And when an answer goes past your material, it says so.** Anything InkVault adds from general knowledge now starts with "Beyond your notes:" and is kept out of anything it cites. Explaining, expanding and comparing all still work — you can just see where your notes end.


## InkVault 0.2.22

### Search is better at whole questions, not just keywords
Typing a real question — "in the vasculitis lecture what were the results about palpable purpura" — used to favour a document's *opening* page: the one that repeats the topic and answers nothing. It won simply by echoing more of your words.

Longer questions now lean on meaning rather than word-counting, and a page that **is** the section you asked for ("results", "limitations", "the dose") is recognised as such. Short keyword searches are untouched — they were already good at what they do.

### Search understands "not"
- "the atorvastatin paper **not** the rosuvastatin one"
- "enoxaparin dose **excluding** version 1"

Previously the excluded document could come back **first**. Now it's pushed down. Works with "not", "without", "excluding", "except" and "other than".

### And what didn't change
Vague one-word searches like "results" or "discussion" still correctly return no confident match. That was checked carefully — the improvements above could easily have broken it, and an early version did.

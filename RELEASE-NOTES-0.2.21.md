## InkVault 0.2.21

### Ask AI answers in about a second, not eight
Every question was going to Gemini Pro — a deep "thinking" model — regardless of what you had chosen.

On the Mac, Settings said answers used the model you picked, and that was simply not true: the code path meant to honour your choice could never run, so picking Flash was discarded on every question.

Measured on a real library, same question, same evidence: **8.1s → 0.8s**.

Retrieval was never the slow part — it was 0.6 seconds of an 8.7-second wait. The model was 93% of it.

### The model picker now names the wait
"2.5 Flash — fastest, about 1s". "Pro latest — deepest, about 8s". Pro is still there and still gives the deepest answer — it's now a choice you make rather than one you discover.

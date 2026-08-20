# InkVault 0.5.0

Study stops being something that vanishes when you close the sheet.

## Study History

Every quiz you finish is kept, with your answers, your score and the marked
paper. Open it from **File ▸ Study History…** (⌘⇧H) or the library's Add menu.

- Reopen the marked paper for any past sitting. No model call, no cost.
- **Retake This Quiz** sits the whole paper again, reshuffled, for nothing.
- Grouped by source, with your best and your average per source, and the topics
  you keep getting wrong.
- The quiz setup screen now shows your record for that source *before* you spend
  a generation on material you have already been tested on.
- Retakes are listed but never counted in an average. A retake sits only what
  you missed, so counting it would report a rising average for a shrinking exam.

## Saved decks

Flashcard decks are kept too, and reopen straight into the Anki footer, so
sending a deck again costs nothing.

## The exam clock is yours

45s, 60s, 90s, 2 minutes, or no clock at all. The default is unchanged at board
pace. The setup screen now quotes the **rate**, because the clock is built from
the questions actually written and the old caption quoted a total based on the
number you asked for.

## Flashcards are checked now

Cards used to carry a citation and nothing that could be verified. Every card
now quotes the verbatim line from your notes that makes its back correct, that
line is checked in code against your actual page, and a card whose quote is not
really there is dropped rather than shown. The quote appears under every card
and travels with the deck into Anki.

## Fixes

- **Quizzes and decks never worked on anything but Gemini.** Both ends of the
  Fast/Best picker sent Gemini model ids to whichever provider you had
  configured, so OpenAI, Claude and OpenRouter users got an API error rather
  than a quiz. Fixed for both.
- The blind verifier could stop marking a large quiz and say nothing. It asked
  for too few tokens, so a long reply was cut off, failed to parse, and rejected
  nothing — verification switched itself off exactly on the biggest papers. It
  now has room, and when it still cannot finish, the paper says so.
- A concept-sliced exam printed one slice's coverage note as if it explained the
  whole paper, and suppressed the sentence counting what actually survived.
- **Retake Missed** was hidden from anyone who missed everything, which is
  precisely when it is worth having.
- A quiz question whose choices read identically could be keyed to the wrong one
  after shuffling.
- Multi-document quizzes cite their sources more reliably: the page markers name
  the file, which is what the citation rule always asked the model to copy.
- Settings are written atomically, and a preference that had been silently
  reverting on every relaunch is kept.

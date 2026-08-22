# InkVault 0.5.12

**Importing a long book no longer makes the app stutter.**

Diagnostics from a real 1633-page import showed the interface hitching almost continuously for the thirteen minutes it ran — 845 stutters, nearly all of them during the import. The cause was a single step that opened the PDF file once per page on the same thread that draws the screen, before handing the actual work off to the background.

That step now runs in the background with everything else. Scrolling, writing and reading stay smooth while a book imports.

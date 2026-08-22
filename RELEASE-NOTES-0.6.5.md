# InkVault 0.6.5

**Books get their table of contents back.**

Two things were wrong, and the first was InkVault's fault. When InkVault makes a document searchable it rebuilds the file to add a text layer, and that rebuild was quietly dropping the book's own table of contents. Every book you have imported lost it that way. It is now saved before the rebuild happens, and books you imported earlier will recover it automatically if the original file is still on your Mac or device.

For scanned books that never had one, InkVault now reads the contents pages the book itself prints — the ones with chapter names and page numbers — and works out how they line up with the file, which is not the same thing because of front matter. On a 402-page orthopaedics text it recovers 56 entries landing on the right pages. Recovered titles are only as good as the scan, so this is used only where there is no real outline to use instead.

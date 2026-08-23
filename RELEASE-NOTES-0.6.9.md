# InkVault 0.6.9

**The long freeze in scanned books is fixed, and it was not what anyone thought.**

Touching a page of a scanned book made iOS start its own text recognition over the page images — on the main thread, page after page. On a long book that took nearly half a minute and well over a gigabyte, which is why it always seemed to happen when you scrolled a long way and then tried to select something.

That work is now switched off in the reader, because InkVault already does it. Reading a page image is what indexing is: done once, with a model, saved to an index that answers instantly. Having iOS repeat it on every touch was paying twice for a worse result.

Four earlier attempts at this fixed real problems — selecting a whole book, drawing surfaces on pages you only scrolled past — but none of them was the cause. It took a diagnostic that could watch the app while it was frozen, and that arrived two releases ago.

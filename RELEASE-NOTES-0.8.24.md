# InkVault 0.8.24

**Marks show the first time you open a document, and the reader uses much less memory.**

**No more closing and reopening.** If the annotations were still downloading when you opened a book, the window missed them and only picked them up the next time. It now waits for its own file and shows them as soon as they land.

**Less memory while reading.** The reader was keeping sixteen pages' worth of pen layers in memory for pages you were not looking at — about 100 MB, and more when zoomed in. It keeps six now, and rebuilding one costs a small file read.

**A large book is no longer held open after saving your marks.** Publishing kept the whole file in memory for the rest of the session; on a big textbook that alone was over a hundred megabytes.

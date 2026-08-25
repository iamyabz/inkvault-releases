# InkVault 0.8.22

**Pages you only drew on — with no tape or sticky note — now sync too.**

Marks were only being sent for pages that also had tape or a card on them. A page with nothing but your handwriting was silently left out, so most of what you wrote never reached your other devices.

It happened because working out a page's size relied on the document's file being on the same device that imported it. On an iPad reading a book imported on a Mac, that lookup failed, and the page was skipped without any error.

If a page ever has to be skipped now, the diagnostic report names it.

# InkVault 0.8.19

**Marks you make on a book that came from another device now reach your other devices.**

If you imported a book on your Mac and then wrote on it on your iPad, those marks could never leave the iPad. Two things were wrong, and both only showed up in exactly that situation:

The annotations were being saved next to wherever the book's file lived — which, for a book imported on the Mac, is a Mac folder that does not exist on an iPad. Saving failed silently.

And even when it worked, the upload only ran for documents whose original file was on the same device. Annotations are their own separate thing and never needed that.

Open the book on the iPad, leave the reader, and the marks will publish on the next sync.

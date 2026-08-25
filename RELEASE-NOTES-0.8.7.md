# InkVault 0.8.7

**Protects your annotations, and makes writing on a page stay fast as it fills up.**

**Zooming could rewrite your ink at the wrong size.** Crossing a zoom threshold saved the page's handwriting back scaled up or down. Introduced in 0.8.6 and fixed here.

**Writing no longer slows down as a page fills.** Each new stroke was re-saving the whole page's handwriting while the pen was still moving, so a busy page got steadily heavier to write on.

**Scrolling a marked-up document is lighter.** The pen layer was being re-laid-out on every movement of the page rather than only when something changed.

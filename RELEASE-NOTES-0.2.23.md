## InkVault 0.2.23

### A page that mentions nothing you searched for no longer outranks one that does
Searching "epistaxis management" returned a heme-catabolism page. Containing **neither** word. Above `Epistaxis.pdf`. It won on semantic similarity alone (blood is, loosely, related to nosebleeds), while the safeguards meant to catch exactly this could only ever affect keyword scoring and never the semantic half.

Now a page missing *all* of your rare search words is pushed down. But only when those words actually exist somewhere in your library. Searches that rely on meaning still work exactly as before: "heart attack" still finds the page that says "myocardial infarction", because there is nothing findable being missed.

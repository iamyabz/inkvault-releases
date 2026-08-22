# InkVault 0.5.10

**You can see what an import is doing now.**

Reading a handwritten note has always been traceable in the diagnostics report: which page, which stage, how long, what came back. Importing a document told you almost nothing — which is why a crash on a very long book took as long as it did to work out. The report could say the app had been busy and how much memory it was using, and nothing about where it had got to.

Imports now record the same detail: what is being read and how big it is, progress and free memory as it goes, every failure with its reason, and a summary at the end of which readers actually did the work and whether any page ended up without a search vector. The step that runs at the very end is bracketed, so if it ever runs a device out of memory the report names it outright.

Detail is kept per-page for shorter documents and summarised for long ones, so a thousand-page book leaves a readable trail instead of burying everything else in it.

You can send the report from Settings ▸ Diagnostics.

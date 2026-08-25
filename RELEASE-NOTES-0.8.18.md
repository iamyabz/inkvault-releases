# InkVault 0.8.18

**Fixes documents disappearing from one device and then from all of them.**

Sync decided that any document it had published but could no longer see locally must have been deleted, and told every other device to remove it. That is right only once the library has actually been read off disk — and reading it is deliberately delayed at launch, so there is a moment when the app legitimately has no documents yet. If a sync ran in that moment, it deleted everything it had ever published.

On this account it moved **59 documents to Recently Deleted** without anyone asking.

Nothing was lost: Recently Deleted keeps records and files intact for thirty days, and they can be restored.

Deletions are now only published once the library has genuinely loaded and is not empty. If sync declines to publish one, it says so in the sync log rather than doing it quietly.

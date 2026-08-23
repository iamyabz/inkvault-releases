# InkVault 0.6.11

**Narrowing the freeze, honestly.**

The diagnostic confirmed two things this time. The app really is doing the work itself rather than waiting on something else, and the explanation in the last release was wrong: it assumed your books had no searchable text and needed the system to find it. They all do have it, so that was never the reason.

This build records which document you opened and, for the two places InkVault uses text recognition, which thread each ran on. That is the last thing standing between the symptom and the cause.

No behavioural change. The last two releases each shipped a fix for a cause that had not been established, and neither worked.

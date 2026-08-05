# InkVault 0.3.0

The first public build.

## No more expiring builds

Every earlier build was a beta build, and beta builds stopped working ten and a
half days after they were made. Not just the paid features: the whole app,
including opening documents you had already added, replaced by an update prompt
until you installed a newer one.

Public builds do not expire on a timer. Nobody gets locked out of their own
library again.

## Terms of Service, on first launch

Mac, iPhone and iPad now show the terms once, before anything else, and ask you
to accept them. Four things are said up front, in plain words:

- This is unfinished software. It can lose work. Keep your own backups.
- Beta access is free and temporary, and it is not a claim on a free or
  discounted licence later.
- AI features run on an API key you supply, so those charges are yours.
- Never use InkVault for clinical, legal or other professional decisions.

## The terms themselves were rewritten

- **Refunds now say who actually issues them.** Apple handles refunds for
  anything bought through the App Store, and we cannot issue one on their
  behalf. The previous wording promised something we had no power to do.
- **One subscription covers Mac, iPhone and iPad** under the same account.
- **The privacy section says exactly what we hold:** your name, your email
  address, a one-way hashed device identifier, your app version, and crash
  reports containing a stack trace. Nothing you ever wrote. Your library stays on
  your devices, and in your own iCloud if you turn sync on, encrypted with a key
  we do not have.
- Added the terms Apple requires of App Store apps, an assignment clause so the
  agreement survives the move to a company, a data rights section covering
  access, correction, deletion and portability, and consumer carve-outs for the
  UK and EEA.

`getinkvault.com/terms` is now generated from the same text the apps show, so
the website and the apps cannot drift apart. They already had.

## Under the hood

Groundwork for accounts and a single subscription that unlocks all three
devices. Nothing user-visible yet.

---

**Requires** macOS 14 or later on Apple Silicon.
Questions: support@getinkvault.com

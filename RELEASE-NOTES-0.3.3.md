# InkVault 0.3.3

## "Update & Relaunch" actually updates

If you have clicked Update & Relaunch and watched InkVault quit, reopen, and
show you the very same update banner, this is why.

The installer verified that the incoming copy was signed by "InkVault Local",
the self-signed certificate used before InkVault was notarized by Apple. Every
release since 0.2.10 has been signed with a proper Developer ID certificate
instead, so that check could never pass again. When it failed the installer did
not warn: it skipped the replacement and reopened the version you already had,
which looks exactly like deciding not to update.

The result is that automatic updates have not worked for anyone since 0.2.10,
and four releases went out that could only be installed by downloading the disk
image by hand.

The check now uses the same signing requirement the app already uses to verify
itself, so it accepts what is actually shipped and still refuses anything else.

**One manual install is needed.** The fix lives in the new version, but the
installer doing the work is the old one, so it cannot repair itself. Download
this release, drag InkVault to Applications, replace the existing copy. Updates
after this one will install on their own.

## The update banner reads properly

It was pasting the entire release-notes document into a single-line banner, so
it appeared as "InkVault 0.3.2 is ready. # InkVault 0.3.2" with the formatting
marks showing. It now shows one clean sentence.

## And it cannot happen quietly again

Publishing a release now runs the updater's own signature requirement against
the disk image that is about to be uploaded, and refuses to publish if the
updater would reject it.

---

**Requires** macOS 14 or later on Apple Silicon.
Questions: support@getinkvault.com

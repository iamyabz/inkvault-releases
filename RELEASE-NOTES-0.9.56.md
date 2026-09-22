# InkVault 0.9.56

A privacy fix for shared files.

## What this fixes

- **A shared `.inkvault` carried the folder it came from.** When you share a
  document, InkVault sends the folder structure you chose to share — and nothing
  above it. A loose document is supposed to carry no folders at all: where it
  sits in your library is your business. One internal field held the full path
  anyway, in readable text, including every parent folder above whatever you
  shared. Anyone you sent a file to could read it.

  Nothing else about sharing changes, and files made by this version open in
  older ones exactly as before.

If you have shared files from an earlier version, the folder names in them are
already out; re-sharing from 0.9.56 produces a clean file.

## Notes

This is a beta build. Keep your own backups of anything you cannot afford to
lose, and do not use InkVault for clinical, legal or other professional
decisions.

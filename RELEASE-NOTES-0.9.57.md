# InkVault 0.9.57

A safety release for your library: every document now keeps one identity
across your devices, deleting is harder to get wrong, and a new version can
never start syncing until you say so.

## Update all your devices

This version updates your iCloud library's sync format. Once one device starts
syncing on 0.9.57, any Mac or iPad still on an older version pauses its sync
("update required") until it is updated. Nothing is deleted. The older version
still opens and edits its library on that device.

## Start Syncing, on your terms

The first time you open 0.9.57, sync waits. A banner asks **Start syncing with
iCloud?** and nothing is sent to or read from iCloud until you press **Start
Syncing**. Choose **Not Now** and your library works normally on that device.
You can start later from Settings.

## Safer deletion

- **Deleted on one device, not lost on another.** When something is deleted on
  another device, you see it under **Deleted on Other Devices** and choose:
  **Keep** it here, or **Delete Here Too**.
- **Deleted items stay deleted.** A document you delete no longer reappears
  because an older copy synced back from another device.
- **Different Apple Accounts stay separate.** A deletion made under one Apple
  Account never removes anything that belongs to another.
- **Free Up All never frees handwriting.** Downloaded files that iCloud can
  supply again are freed. Your ink, Tape and sticky notes always stay on the
  device.

## Imports that can't go wrong silently

If an imported file would collide with something already in your library, it is
set aside instead of overwriting anything. Find it under **Set-Aside Imports**,
then **Import as New** or **Discard**. The rest of the queue carries on.

## Also

- Documents are tracked more carefully across devices, so annotations, tables
  of contents and study history stay with the right document.
- A book's own table of contents now reaches your other devices.

## Notes

This is a beta build. Keep your own backups of anything you cannot afford to
lose, and do not use InkVault for clinical, legal or other professional
decisions.

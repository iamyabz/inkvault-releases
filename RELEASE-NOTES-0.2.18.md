## InkVault 0.2.18

### You can stop an import
A long document is minutes of work, and until now there was no way out of it once started. There's now an ✕ on the progress banner wherever you are in the app, and a **Stop Import** button on the import screen.

Pages already read are kept, they're indexed and paid for, so stopping never costs you what you'd already gained.

On the Mac, the ✕ on the indexing banner has always been there but only ever stopped *document* scans. Audio, video, YouTube and spreadsheet imports ignored it: the banner cleared while the work carried on in the background. All four now stop when you ask them to.

### iPhone/iPad: file pickers that open
"Choose Files" and "Choose a Recording" could silently do nothing. Four separate pickers were attached to one screen, and iOS resolves that by presenting one of them and ignoring the rest. So which buttons worked depended on the device. There's now a single picker that knows what it was asked for, and every kind accepts multiple files at once.

### A clearer reason when importing is blocked
Without a Gemini API key the Choose Files button is disabled, which is indistinguishable from broken. It now says what's missing, right where you tap.

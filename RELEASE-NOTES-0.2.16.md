## InkVault 0.2.16

### Whisper now transcribes the language you actually spoke
On both Mac and iPhone/iPad, Whisper was being told to decode in English no matter what it heard — so Urdu, Arabic, Spanish, or any other language came out as a rough English translation instead of a transcript. It now listens first and transcribes in the language it detects, per 30-second window, so a lecture that switches languages mid-sentence follows along. Nothing to configure.

This is also why the model list used to say "for Arabic/Urdu use Gemini" — the multilingual model was never being allowed to be multilingual. That caveat is gone because the limitation is gone.

### No more `<|startoftranscript|>` garbage in recordings
Whisper's internal control tokens were leaking into transcripts as if they were speech — a silent stretch could produce a whole "page" of markup that then polluted search. They're stripped now, and a segment that was only markup is dropped instead of indexed. If a recording already imported with the garbage, re-transcribe it and it comes out clean.

### A multilingual Small model on the Mac (~488 MB)
Multilingual transcription no longer requires the 1.6 GB Large v3 Turbo download.

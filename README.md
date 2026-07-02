# InkVault

> Search your handwritten notes, PDFs, and recordings like they were typed.

**InkVault** is a native macOS app that turns your handwritten notes, scanned PDFs,
lecture recordings, spreadsheets, and documents into one **private, AI-searchable**
knowledge base — with exact **page and timestamp citations**. Everything is indexed
on your Mac.

## ⬇️ Download

**[Download the latest version](../../releases/latest)** → grab the `.dmg`.

## Features
- 📄 Handwriting, scanned PDFs, and printed docs — OCR'd and searchable
- 🎙️ Audio & lectures — transcribed with click-to-seek timestamps
- 📊 Spreadsheets — rows indexed and answerable
- 🔎 Hybrid local search with ranked evidence cards
- ✨ **Ask AI** — cited answers as a concise answer, key points, or study notes
- 🔒 Local-first & private — your files never leave your Mac
- ⌨️ Global ⌃⌥Space command bar

## Requirements
- macOS 14 (Sonoma) or later
- A free **Google Gemini API key** ([get one](https://aistudio.google.com/apikey)) for OCR, transcription, and Ask AI. Search works locally.

## Install
1. Open the `.dmg` and drag **InkVault** into **Applications**.
2. **First launch:** right-click InkVault → **Open** → **Open** (it's not from the App Store, so macOS asks once).
   - If it ever says "damaged," run in Terminal: `xattr -dr com.apple.quarantine /Applications/InkVault.app`
3. Open **Settings (⌘,) → AI Model** and paste your Gemini key.

## Trial & licensing
Free for **14 days**, full features, no code needed. After that InkVault stays open
in **read-only** (you can still view and search your library) until you enter a
license code.

## Privacy
Your files, extracted text, search index, and API keys stay **on your Mac**. Only
the specific evidence for a question — never your whole library — is sent to Gemini
(with your key). No accounts, no tracking. See the in-app Privacy panel for details.

## Support
Questions or bugs: **asim.j.mohamed@gmail.com** · Website: (coming soon)

---
© 2026 Abbas Mohamed. All rights reserved. InkVault is proprietary software; see [LICENSE](LICENSE).

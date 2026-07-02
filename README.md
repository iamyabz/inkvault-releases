<p align="center">
  <img src="assets/icon.png" width="128" alt="InkVault icon" />
</p>

<h1 align="center">InkVault</h1>

<p align="center">
  <b>Search your handwritten notes, PDFs, and recordings like they were typed.</b>
</p>

<p align="center">
  A native macOS app that turns handwritten notes, scanned PDFs, lecture recordings,
  spreadsheets, and documents into one <b>private, AI-searchable</b> library —
  with exact <b>page and timestamp citations</b>. Everything is indexed on your Mac.
</p>

<p align="center">
  <a href="../../releases/latest"><img src="https://img.shields.io/github/v/release/iamyabz/inkvault-releases?label=Download&color=6C4BD8&style=for-the-badge" alt="Download latest"></a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/macOS-14%2B-1d1d1f?logo=apple&logoColor=white" alt="macOS 14+">
  <img src="https://img.shields.io/github/downloads/iamyabz/inkvault-releases/total?color=2ea44f&label=downloads" alt="Downloads">
  <img src="https://img.shields.io/badge/license-proprietary-lightgrey" alt="License">
</p>

---

## ✨ Features
- 📄 **Handwriting, scans & printed docs** — OCR'd and searchable
- 🎙️ **Audio & lectures** — transcribed with click-to-seek timestamps
- 📊 **Spreadsheets** — rows indexed and answerable
- 🔎 **Hybrid local search** with ranked evidence cards
- 🧠 **Ask AI** — cited answers as a **concise answer**, **key points**, or **study notes**
- 🔒 **Local-first & private** — your files never leave your Mac
- ⌨️ **Global ⌃⌥Space command bar** — search from any app

## ⬇️ Download
Grab the latest `.dmg` from the **[Releases page](../../releases/latest)**.

> 🌐 **Website:** _coming soon_ — a one-click download page is on the way. <!-- TODO: replace with https://inkvault.app once live -->

**Requirements:** macOS 14 (Sonoma)+ · a free [Google Gemini API key](https://aistudio.google.com/apikey) for OCR, transcription, and Ask AI (search works locally).

## 🚀 Install
1. Open the `.dmg` and drag **InkVault** into **Applications**.
2. **First launch:** right-click InkVault → **Open** → **Open** (macOS asks once, since it's not from the App Store).
   - If it ever says *"damaged,"* run in Terminal: `xattr -dr com.apple.quarantine /Applications/InkVault.app`
3. Open **Settings (⌘,) → AI Model** and paste your Gemini key.

## 🎟️ Trial & licensing
Free for **14 days** — full features, no code needed. After that InkVault stays open in
**read-only** (you can still view and search your library) until you enter a license code.

## 🔐 Privacy
Your files, extracted text, search index, and API keys stay **on your Mac**. Only the
specific evidence for a question — never your whole library — is sent to Gemini (with
your key). No accounts, no tracking.

## 💬 Support
Questions or bugs: **abbas.j.mohamed@gmail.com**

---
<p align="center"><sub>© 2026 Abbas Mohamed. All rights reserved. InkVault is proprietary software — see <a href="LICENSE">LICENSE</a>.</sub></p>

<p align="center">
  <img src="assets/autocut-banner.svg" alt="KLIK AutoCut: raw takes in, a clean cut out, in Premiere. Closed beta." width="1200">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/status-closed%20beta-FF7A3D?style=flat-square" alt="Closed beta">
  <img src="https://img.shields.io/github/v/release/t3knobox/klik-autocut-releases?include_prereleases&label=newest%20version&style=flat-square&color=2b2d33" alt="Newest version">
  <img src="https://img.shields.io/badge/Premiere%20Pro-2026-2b2d33?style=flat-square" alt="Premiere Pro 2026">
</p>

<p align="center">
  <a href="#install">Install</a> &nbsp; / &nbsp;
  <a href="#what-it-does">What it does</a> &nbsp; / &nbsp;
  <a href="#what-you-need">What you need</a> &nbsp; / &nbsp;
  <a href="https://github.com/t3knobox/klik-autocut-releases/releases">Releases</a>
</p>

> [!IMPORTANT]
> **KLIK AutoCut is in a closed beta.** Anyone can download it, but it only opens with a **beta key from KLIK**. If you're one of our testers, your key is on its way to you.

## Install

<p>
  <a href="https://github.com/t3knobox/klik-autocut-releases/releases/latest/download/KLIK-AutoCut-Setup.exe"><img src="assets/download-windows.svg" alt="Download KLIK AutoCut for Windows" width="380"></a>
  &nbsp;
  <a href="#on-a-mac"><img src="assets/download-macos.svg" alt="KLIK AutoCut for macOS: Apple silicon, set up with KLIK" width="380"></a>
</p>

[Release notes & checksums](https://github.com/t3knobox/klik-autocut-releases/releases/latest)

### On Windows

1. **Download** the installer with the orange button (`KLIK-AutoCut-Setup.exe`).
2. **Open it.** If Windows says it protected your PC, choose **More info**, then **Run anyway**. It installs just for you, with no administrator password.
3. **Sign in with your beta key.** Paste the key KLIK sent you and choose **Sign in**. You only do this once.
4. **Connect your accounts** on the Connections screen: Claude and ElevenLabs. Keys stay in Windows Credential Manager.

<p align="center">
  <img src="assets/screens/signin-dark.png" alt="KLIK AutoCut's first screen: Sign in with your beta key, marked Closed beta" width="560">
</p>

<details>
<summary><strong>Windows protected your PC: why, and is it safe?</strong></summary>

<br>

The beta installer isn't code-signed yet, so Windows SmartScreen doesn't recognise the publisher. Choose **More info → Run anyway**. Every release lists the installer's SHA-256 in `SHA256SUMS.txt`; to compare, run `Get-FileHash .\KLIK-AutoCut-Setup.exe` in PowerShell.

</details>

### On a Mac

The Mac beta runs alongside the AutoCut add-on for Premiere, and KLIK sets it up with you (Apple silicon only). There's no Mac installer to download yet. Ask your KLIK contact and we'll get you going in a short call.

## Updates

AutoCut checks this page for a new version each time it opens.

- **Windows:** when one is out, an **Update** button shows at the top with what changed. One click downloads it, checks it against the release's checksum, installs it and opens AutoCut again. Your episodes and settings stay as they are.
- **Mac:** AutoCut updates with the add-on: **Settings → Connections → AutoCut add-on → Update**, then reopen the app.

You can check any time from **Settings → About → Check for updates**. Every release's notes are on the [releases page](https://github.com/t3knobox/klik-autocut-releases/releases).

## What it does

AutoCut turns talking-head raws into a tidy edit inside your own Premiere project, then gets out of the way so you can finish it.

<p align="center">
  <img src="assets/how-it-works.svg" alt="Three steps: cut the A-roll, place the B-roll, subtitles and finish" width="1200">
</p>

- **Cuts the A-roll.** It transcribes the raws, removes retakes and false starts, and keeps the last complete take. You check it as a **paper edit**: read it like a script, play any line, bring back anything it cut, or tell it in plain words what to change.
- **Joins it properly.** J-cuts and audio crossfades at every join, in your sequence, so it sounds edited, not chopped.
- **Places B-roll from your own footage.** Make a **Library** of your footage folders and search it in plain words ("sunset over the bridge"). Auto B-roll suggests a shot for each moment; swap any of them, then **Place all**. Talking-to-camera clips never become B-roll.
- **Writes the subtitles** from the same transcript, timed to the cut, onto a captions track.
- **Leaves you in charge.** It edits a working copy of your raws sequence, never writes to shared drives like LucidLink, and any step can be stopped.

## What you need

| | |
| --- | --- |
| **Computer** | Windows 10 or 11 (64-bit), or a Mac with Apple silicon |
| **Premiere Pro** | 2026, with the AutoCut add-on (KLIK helps you set it up) |
| **Claude** | Your own Claude subscription, signed in through Claude Code. AutoCut uses it to read the transcript and plan the edit |
| **ElevenLabs** | An API key with Speech to Text access, for transcripts. Transcripts use that account's credits |
| **Beta key** | From KLIK. You'll need it to sign in the first time |
| **Optional** | Cloudflare R2, to keep Library books in the cloud |

**Windows and Mac do the same edits.** One part stays on the Mac for now: tagging new footage into a Library book uses a model that needs Apple silicon. Books tagged on a Mac and put in the cloud work fully on Windows.

## Help

Something not right? Tell your KLIK contact what you were doing and what you saw, and include your version from **Settings → About**. Lost your key, or need one for a new teammate? Ask KLIK for a new one.

---

<details>
<summary><strong>About this repository</strong></summary>

<br>

This is KLIK AutoCut's public home for installers, release notes and update files. Each release carries the Windows installer (`KLIK-AutoCut-Setup-<version>.exe`, and the same file as `KLIK-AutoCut-Setup.exe` for the button above), `latest.json` and its signature, which the app checks before offering an update, and `SHA256SUMS.txt`. `revoked.json` lists beta keys that no longer work.

The application source is kept in a separate private repository. GitHub's automatic **Source code** archives contain only this page's files, not the app.

</details>

<p align="center"><sub>© KLIK Creatives. Closed beta: features and requirements may change between releases.</sub></p>

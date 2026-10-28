# Aegis Camera

A camera app for **Xperia devices**, with its own photo processing: multi-frame HDR+ and
Super-res merges, photo styles, Pro Photo and Pro Video controls, and 4K / 1080p / 720p video.

> **Beta.** Aegis is in public beta: expect bugs, and back up photos and videos that matter.
> This repository holds the app's releases and bug reports only; the source code is not public.

## Download

**[Latest release →](https://github.com/Unagi-sann/AegisCam-releases/releases)**

Every release has `AegisCamera.apk` and its SHA-256 checksum (`AegisCamera.apk.sha256`).

## Install

1. On the phone, open the latest release and download **AegisCamera.apk**.
2. Open the downloaded file. The first time, Android asks to allow installs from your browser or
   file manager: allow it, go back, and open the file again.
3. Open **Aegis Camera** and allow the camera (and microphone, for video sound).

**Updating:** install the new APK over the old one: your settings are kept. Aegis tells you when a
new version is out (Settings ▸ Misc. ▸ About & support ▸ Check for updates; you can turn it off).

**Checking the download (optional):** on a computer, `sha256sum AegisCamera.apk` should print the
value in `AegisCamera.apk.sha256` and the release notes.

## Phones

| Phone | Status |
| --- | --- |
| Sony Xperia 5 II (XQ-AS42, XQ-AS52, XQ-AS62, XQ-AS72, SO-52A, SOG02, A002SO) | Tested |
| Sony Xperia 1 II (XQ-AT51, XQ-AT52 and other regions) | Being added: lenses fixed in 1.1-beta4, testing with a tester |
| Sony Xperia 1 V (XQ-DQ54 and other regions) | Being added: lens zoom and RAW fixes in 1.1-beta4, testing with a tester |
| Google Pixel 10 Pro XL | Being added: lens buttons fixed in 1.1-beta4, testing with a tester |
| OnePlus 12 (CPH2573 and other regions) | Being added: ultra wide and main only (OnePlus keeps the telephoto for allow-listed apps) |
| Sony Xperia 1 III (XQ-BC72, SOG03 and other regions) | Being added: lens fix (depth sensor) in 1.1-beta4; 105 mm telephoto position in 1.1-beta15; not tested on the phone yet |
| Sony Xperia 5 III (XQ-BQ42 and other regions) | Not tested yet: same 70 / 105 mm telephoto as the 1 III (105 mm from 1.1-beta15, if the phone reports it) |
| Sony Xperia 1 IV (SO-51C, XQ-CT54 and other regions) | Not tested yet: same camera layout as the 1 V, telephoto zooms optically (85–125 mm) |
| Sony Xperia 1 VI (XQ-EC44 and other regions) | Not tested yet: same camera layout as the 1 V, telephoto zooms optically (85–170 mm) |
| Sony Xperia 5 IV (XQ-CQ72 and other regions) | Not tested yet: ultra wide, main and a fixed 60 mm telephoto |
| Sony Xperia 5 V (XQ-DE72 and other regions) | Not tested yet: ultra wide and main only (no telephoto; 2× is a crop of the main) |
| Sony Xperia 1 (J9110 and other regions) | Not tested yet: 2019 camera software (Android 11 at most), so lens switching may differ; the ultra wide has fixed focus |
| Other Android phones (Android 10 or newer) | Untested: may install, but lenses or modes may not work |

Have another phone? You can help add support: in Aegis, open **Settings ▸ Misc. ▸ Export camera
capabilities**, then open a **[Support for my phone](https://github.com/Unagi-sann/AegisCam-releases/issues/new/choose)**
request and attach the zip. More ways to help, with every step: **[ADD-A-PHONE.md](ADD-A-PHONE.md)**.

## Report a problem

In Aegis: **Settings ▸ Misc. ▸ Report a problem**. It saves a diagnostics zip in
Documents/AegisCamera and opens the bug report form here: attach the zip and describe what
happened.

Or open a **[bug report](https://github.com/Unagi-sann/AegisCam-releases/issues/new/choose)** directly.
Please check the open issues first.

## Legal

- [Beta licence (EULA)](LICENSE.md): free to use; don't re-upload or modify the app.
- [Privacy](PRIVACY.md): Aegis collects nothing.
- [Third-party notices](THIRD-PARTY-NOTICES.md): open-source components in the app.

Aegis Camera is an independent app, not affiliated with Sony. Sony and Xperia are trademarks of
Sony Group Corporation.

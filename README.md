# AegisCam
A camera project geared towards improving the overall experience on older hardware, with improved auto modes, HDR+, and modern features. Currently geared towards Xperia devices, with more support planned with later builds.

Currently built and tested on the **Sony Xperia 5 II**, with its own photo processing: multi-frame HDR+ and
Super-res merges, photo styles, Pro Photo and Pro Video controls, and 4K / 1080p / 720p video.

> **Beta.** Aegis is in public beta: expect bugs, and back up photos and videos that matter.
> This repository holds the app's releases and bug reports only; the source code is not public.

Full Disclosure: AI tools have been used while building this app.

## Download

**[Latest release →](https://github.com/Unagi-sann/AegisCam-releases/releases)**

Every release has `AegisCamera.apk` and its SHA-256 checksum (`AegisCamera.apk.sha256`).

## Notable features

1. Faster auto mode, with HDR+ support (Aegis Experimental)
2. 4k60fps video working on the 5ii with portrait mode
3. Option to turn on level and grids
4. Working camera button, same as photo pro. Also works in video mode.
5. Seamless lens switching
6. HDR+ based on Google's public documentation
7. Custom bitrates for video modes
8. Easy diagnostics export for debugging and support
9. GPU merge for HDR+, with improvements planned
10. Filters for pictures with strength sliders

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
| Other Android phones (Android 11 or newer) | Untested: may install, but lenses or modes may not work |

Have another phone? You can help add support: in Aegis, open **Settings ▸ Misc. ▸ Export camera
capabilities**, then open a **[Support for my phone](https://github.com/Unagi-sann/AegisCam-releases/issues/new/choose)**
request and attach the zip. More ways to help, with every step: **[ADD-A-PHONE.md](ADD-A-PHONE.md)**.

## Report a problem

In Aegis: **Settings ▸ Misc. ▸ Report a problem**. It saves a diagnostics zip in
Documents/AegisCamera and opens the bug report form here: attach the zip and describe what
happened.

Or open a **[bug report](https://github.com/Unagi-sann/AegisCam-releases/issues/new/choose)** directly.
Please check the open issues first.

## Commands for full logcat directly from the app (optional)

1. Install adb and fastboot tools on your PC depending on your OS.
2. Connect your device with adb.
3. Run these commands (one time only) -

adb shell pm grant com.vista.camera android.permission.READ_LOGS

adb shell pm grant com.vista.camera android.permission.DUMP

adb shell am force-stop com.vista.camera

After this, Aegis will be able to save logcat files along with the already included diagnostics. This gives us a better understanding of camera functionality for your specific device. 

## Legal

- [Beta licence (EULA)](LICENSE.md): free to use; don't re-upload or modify the app.
- [Privacy](PRIVACY.md): Aegis collects nothing.
- [Third-party notices](THIRD-PARTY-NOTICES.md): open-source components in the app.

Aegis Camera is an independent app, not affiliated with Sony. Sony and Xperia are trademarks of
Sony Group Corporation.

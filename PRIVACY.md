# Aegis Camera Privacy Notice

Effective 24 October 2026

**Short version: Aegis Camera collects no personal data, has no accounts, ads, analytics or
tracking, and sends nothing about you anywhere.**

## Photos and videos

Photos and videos are processed on the phone and saved to the phone's own storage
(Pictures / Movies / DCIM). Aegis never uploads them.

## Permissions

| Permission | Used for |
| --- | --- |
| Camera | Taking photos and videos |
| Microphone | Sound in videos (only while recording) |
| Photos and videos (media) | Showing your last photo or video as the gallery thumbnail |
| Vibration | Haptic feedback |
| Internet | Only the optional update check (below) |

## Update check

If **Check for updates** is on (Settings ▸ Misc. ▸ About & support; on by default), Aegis reads
the public list of releases from GitHub at most every 12 hours
(`api.github.com/repos/Unagi-sann/AegisCam-releases/releases`). The request contains nothing about
you or your photos. Like any website, GitHub receives your IP address and an app identifier
("AegisCamera"); see [GitHub's privacy statement](https://docs.github.com/site-policy/privacy-policies/github-general-privacy-statement).
Turn the setting off and Aegis makes no network requests at all.

## Diagnostics and camera capability exports

**Export diagnostics**, **Report a problem** and **Export camera capabilities** save a zip file
to Documents/AegisCamera **on your phone only**. Nothing is sent automatically. The zip leaves
your phone only if you choose to attach it to a report or send it to someone.

These files can contain: phone model, Android version and firmware; camera and lens details;
Aegis's settings; app logs, crash reports and photo processing reports. If you granted the extra
log permissions over ADB, they can also include the phone's system log, which may mention other
apps. They don't contain your photos or videos. Look through a zip before sharing it if unsure.

Reports you open on GitHub, and files you attach to them, are public.

## Children

Aegis isn't directed at children and collects no data from anyone.

## Changes

Changes to this notice come with a new release and are shown in this file.

Questions: open an issue at <https://github.com/Unagi-sann/AegisCam-releases/issues>.

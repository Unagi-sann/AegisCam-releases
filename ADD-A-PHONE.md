# Help add support for your phone

Aegis is tuned on the Sony Xperia 5 II. Getting another phone to work well needs details only
that phone can give. **Step 1 is enough to start**; steps 2 to 5 help a lot but are optional.

Everything here stays on your phone or computer until you attach it to a
**[Support for my phone](https://github.com/Unagi-sann/AegisCam-releases/issues/new/choose)**
request. Attachments there are public, and GitHub accepts files up to 25 MB each (zip larger
sets, or split them over several comments).

## 1. Export camera capabilities (in the app)

In Aegis: **Settings ▸ Misc. ▸ Diagnostics ▸ Export camera capabilities**. It runs a short lens
test and saves `capabilities_<model>_<time>.zip` in **Documents/AegisCamera**. Attach that zip.

If something goes wrong (an error, a frozen viewfinder, a missing lens), also do
**Settings ▸ Misc. ▸ Export diagnostics** straight after it happens and attach that zip too.

## 2. Set up ADB (once, for steps 3 and 4)

ADB is Google's tool for talking to an Android phone from a computer over USB.

1. Install it on the computer:
   - **Windows / macOS / Linux:** download
     [SDK Platform-Tools](https://developer.android.com/tools/releases/platform-tools) and unzip
     it; run the commands below from that folder (on Windows: `adb.exe`, in Command Prompt or
     PowerShell; on macOS / Linux: `./adb` if `adb` isn't found).
   - **Fedora:** `sudo dnf install android-tools` · **Ubuntu / Debian:** `sudo apt install adb`
     · **macOS (Homebrew):** `brew install android-platform-tools`
2. On the phone: **Settings ▸ About phone**, tap **Build number** 7 times (Developer options
   unlock), then **Settings ▸ System ▸ Developer options ▸ USB debugging** on.
3. Connect the USB cable and run `adb devices`. Tap **Allow** on the phone. The phone should be
   listed as `device`.

## 3. Fuller logs in Aegis's exports

By default an export holds only Aegis's own log. Run these once, then close and reopen Aegis:

```
adb shell pm grant com.vista.camera android.permission.READ_LOGS
adb shell pm grant com.vista.camera android.permission.DUMP
adb shell am force-stop com.vista.camera
```

Aegis then shows *Full system log and camera dump: included* (Settings ▸ Misc. ▸ Diagnostics),
and every export adds the camera service's log and state. Repeat step 1 after this.

These logs can mention other apps on your phone; look through a zip before attaching it if
unsure. Uninstalling Aegis removes the permissions.

## 4. The phone's own camera app in use

This shows how the phone maker's camera app drives the cameras. For each mode below: open the
phone's camera app, start the mode (for video: start recording) and, **while it runs**, on the
computer:

```
adb shell dumpsys media.camera > maker_<mode>.txt
adb logcat -b all -d > maker_<mode>_log.txt
```

Replace `<mode>` with a name, e.g. `photo`, `photo_tele`. Modes, as far as the app has them:

- photo, on each lens (ultra wide, wide, telephoto)
- burst (hold the shutter)
- a long exposure (manual mode, 1 s or longer)
- 4K 60 fps video
- slow motion

Zip all the files and attach them.

## 5. Photos for tuning (optional)

- **Dark frames:** in Aegis **Pro Photo** with the format set to **RAW**, on each lens: cover the
  lens fully and shoot at ISO 100, 800, 3200 and the highest, at 1/60 s.
- **Flat field:** on each lens, an evenly lit white wall, slightly out of focus, at low ISO.
- **Reference pairs:** the same few scenes (daylight, indoors, low light) from the phone's own
  camera app and from Aegis.

The RAW files are in Pictures (or DCIM) under AegisCamera. Zip them per lens.

## Custom or regional firmware

Say so in the request, with the model your phone was sold as. A different region's firmware for
the same phone (for example XQ-AT51 firmware on an XQ-AT52) is fine: the cameras are the same.

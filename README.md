# WEBO

## Your anime and manga, ready when you are.

Discover a title, choose an episode or chapter, and keep your collection on your
own device. WEBO brings a focused player, manga reader, download manager, and
organized local library together in one app.

![WEBO homepage — real application screenshot](https://github.com/Ahmed-02-amr/WEBO/releases/download/v0.2.8/WEBO_homepage.png)

## Download v0.2.8

| Platform      | Package                      | Download                                                                                                               |
| ------------- | ---------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| Windows x64   | Installer · 77.9 MB          | [Download setup](https://github.com/Ahmed-02-amr/WEBO/releases/download/v0.2.8/WEBO_0.2.8_x64-setup.exe)               |
| Windows x64   | Portable ZIP · 102.4 MB      | [Download portable](https://github.com/Ahmed-02-amr/WEBO/releases/download/v0.2.8/WEBO_0.2.8_windows_x64_portable.zip) |
| Android ARM64 | Direct-install APK · 40.6 MB | [Download APK](https://github.com/Ahmed-02-amr/WEBO/releases/download/v0.2.8/WEBO_0.2.8_android_arm64.apk)             |

[Release notes and previous versions](https://github.com/Ahmed-02-amr/WEBO/releases)

Windows packages are unsigned and may trigger an unknown-publisher warning.
The Android APK is an **optimized, debug-signed QA build** for Android 7.0+ on
ARM64 devices. It is not a Play Store release.

## What's new

- **Android startup repair:** initialize HTTPS certificate verification before
  the app starts, and include its required Android component.
- **A much smaller APK:** 40.6 MB instead of 346.2 MB—about 88% smaller—through
  optimized native code and removal of debug symbols.
- **Independent local reading and playback:** opening local media no longer
  waits for the torrent service. Direct manga downloads do not need peers.
- **Faster episode-file discovery:** inspect torrent metadata without starting
  peer discovery; stalled metadata requests return a retryable error.
- **Better Windows packaging:** both packages now include the WebView2 loader
  required by the executable.

This release also includes the recent library autoplay, watched/paused status,
next-downloaded-episode playback, torrent pause/resume, streamlined episode
selection, and absolute episode-numbering fixes.

## Make yourself at home

- Browse live trending, seasonal, and all-time popular anime recommendations.
- Pick a title, then an episode or chapter, before viewing download options.
- Select multiple episodes or chapters when preparing a collection.
- Resume from your local library, with watched and in-progress indicators.
- On Windows, switch audio/subtitle tracks and adjust subtitle appearance in a
  focused player with fading controls.
- Read manga with RTL/LTR modes, fit controls, zoom, bookmarks, and arrow-key paging.
- Manage torrent downloads with progress, peer/speed information, pause/resume,
  deletion, and related-installment discovery.

## Install or update

**Windows:** close WEBO and run the installer. For portable use, extract the whole
ZIP and launch `WEBO.exe`; keep `WebView2Loader.dll` and the `ffmpeg` folder beside
it. Microsoft Edge WebView2 Runtime is required.

**Android:** open the APK on your ARM64 device and allow installation from the app
you use to open it when prompted. Install over the existing WEBO app to preserve
your library and settings. The signing certificate matches the v0.2.4 APK.
**Do not uninstall or clear app data just to update.**

## Testing and current limitations

The release passes 110 automated tests plus TypeScript, Rust formatting, and
Clippy checks. APK verification checks the signature, version, ARM64 ABI, TLS
components and initialization order, and 16 KB alignment.

No Android device or emulator was attached during this release's validation, so
on-device startup, HTTPS requests, downloads, and playback still need confirmation.
The APK does not include the desktop FFmpeg runtime: video conversion and some
audio/subtitle handling remain limited on Android. Manga reading does not require
FFmpeg. Direct manga transfers do not currently support pause/resume.

Catalog metadata and downloads depend on third-party availability. Download
speeds also depend on your network and, for torrents, the available peers.

## SHA-256 checksums

```text
4FE5F649BC9F8975EAC690C8571D8046E2D539BE2C69F6140672EBC6973BE6ED  WEBO_0.2.8_x64-setup.exe
B064AEA236AE94D4C998A1FC861886490FA3081BCD97BEA8BDC4DF1DE33AD764  WEBO_0.2.8_windows_x64_portable.zip
A75853AAB3183A2340209A12BD3E4E1F5E4D960F1FDA6E2E815C3A602FE70580  WEBO_0.2.8_android_arm64.apk
```

## About this repository

This is the official **binary download repository**. It contains this README;
installers, portable packages, APKs, and the real homepage screenshot are attached
to GitHub Releases. Development source code is intentionally not published here.

Found a problem? [Open an issue](https://github.com/Ahmed-02-amr/WEBO/issues) with
your app version, device/OS, and the steps or error message. Please omit personal
data and credentials from screenshots and logs.

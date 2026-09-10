# WEBO

## Your anime and manga, ready when you are.

Discover a title, choose an episode or chapter, and keep your collection on your
own device. WEBO brings a focused player, manga reader, download manager, and
organized local library together in one app.

![WEBO homepage — real application screenshot](https://github.com/Ahmed-02-amr/WEBO/releases/download/v0.2.8/WEBO_homepage.png)

## Download Windows v0.2.9

| Platform    | Package                 | Download                                                                                                               |
| ----------- | ----------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| Windows x64 | Installer · 77.8 MB     | [Download setup](https://github.com/Ahmed-02-amr/WEBO/releases/download/v0.2.9/WEBO_0.2.9_x64-setup.exe)               |
| Windows x64 | Portable ZIP · 105.0 MB | [Download portable](https://github.com/Ahmed-02-amr/WEBO/releases/download/v0.2.9/WEBO_0.2.9_windows_x64_portable.zip) |

**Android is temporarily unavailable.** All APK downloads have been withdrawn
following an on-device “error communicating with nyaa.si” failure. A replacement
will be offered only after the issue is fixed and Android networking and downloads
are verified on-device.

[Release notes and previous versions](https://github.com/Ahmed-02-amr/WEBO/releases)

Windows packages are unsigned and may trigger an unknown-publisher warning.

## What's new in v0.2.9

- **Quiet background media processing:** FFmpeg and ffprobe no longer open console
  windows over the player during probing, thumbnail creation, subtitle extraction,
  audio switching, or video conversion. Error reporting remains available.

Earlier improvements retained:

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
- Switch audio/subtitle tracks and adjust subtitle appearance in a focused player
  with fading controls.
- Read manga with RTL/LTR modes, fit controls, zoom, bookmarks, and arrow-key paging.
- Manage torrent downloads with progress, peer/speed information, pause/resume,
  deletion, and related-installment discovery.

## Install or update on Windows

Close WEBO and install over the current version; no uninstall or data reset is
required. For portable use, extract the whole ZIP and
launch `WEBO.exe`; keep `WebView2Loader.dll` and the `ffmpeg` folder beside it.
Microsoft Edge WebView2 Runtime is required.

## Testing and current limitations

The v0.2.9 release passed 112 automated tests plus TypeScript, Rust formatting,
and Clippy checks, including Windows console-window suppression and real FFmpeg
media processing. Package versions, bundled files, and checksums were verified.
Clean-machine installation and interactive playback QA were not performed for
this patch. Android builds remain withdrawn.

The experimental VPN integration is **not included** in v0.2.9. This release does
not add VPN protection or fix VPN relay connection errors.

Direct manga transfers do not currently support pause/resume. Catalog metadata
and downloads depend on third-party availability. Download speeds also depend
on your network and, for torrents, the available peers.

## SHA-256 checksums

```text
108CAE53085D86CA25787E3D26E8EB4B1D84FFF776B65B21111D6CEAA73EBAD1  WEBO_0.2.9_x64-setup.exe
6716D51F325E8AD29DD8C181B89345FDE3B24F559270B8B2224E654643531639  WEBO_0.2.9_windows_x64_portable.zip
```

## About this repository

This is the official **binary download repository**. It contains this README;
Windows installers, portable packages, and the real homepage screenshot are
attached to GitHub Releases. Development source code is intentionally not
published here.

Found a problem? [Open an issue](https://github.com/Ahmed-02-amr/WEBO/issues) with
your app version, device/OS, and the steps or error message. Please omit personal
data and credentials from screenshots and logs.

# StreamPocket releases

Public downloads, release notes and released source snapshots for StreamPocket.
The ongoing development repository and its history are private. Source snapshots
of distributed versions are supplied here to recipients under the app's GPL-3.0
license; the private development repository is not needed to obtain those snapshots.

## Current status

- [Download StreamPocket 1.0.2](https://github.com/zohaibhassan64/StreamPocket-releases/releases/download/v1.0.2-test.3/StreamPocket-1.0.2.apk)
- [Release notes, source archives and checksums](https://github.com/zohaibhassan64/StreamPocket-releases/releases/tag/v1.0.2-test.3)
- [Public update metadata](https://raw.githubusercontent.com/zohaibhassan64/StreamPocket-releases/main/update.json)

The first release is an **Android test build**, not a production/store release.
It supports Android 10+ on arm64-v8a and x86_64 devices. See the release notes for
what was tested and what still needs phone verification.

Download APKs only from the [Releases page](https://github.com/zohaibhassan64/StreamPocket-releases/releases).
Install updates over the existing StreamPocket app when the signing identity
matches. Do not uninstall first if you want to keep local app history.

## Source and licenses

Each release includes the matching StreamPocket application source archive,
license/notices, checksums, and pinned upstream wrapper/engine source archives.
The source archive includes Gradle launchers and the dependency lock file.
It excludes private Git history, local SDK paths, signing keys and credentials.
Read SOURCE_INFORMATION.md and the source package's THIRD_PARTY_NOTICES.md for
native dependencies, build instructions and upstream sources.

Use the explicitly named **StreamPocket-…-source.zip** release asset for the
application source. GitHub's automatic "Source code" ZIP/tarball contains this
release-catalog repository, not the application project.

## Two kinds of update

- The current app automatically checks for **yt-dlp engine** updates when used,
  at most once per day. This maintains the downloading engine.
- A **StreamPocket APK** update changes the app itself. Version 1.0.1 detects newer
  APKs in Home and Settings. Users choose Download and Install, and Android confirms
  installation. The APK checksum, identity, version and signing certificate are
  checked first. Install this first updater-enabled version manually once.

Public update metadata is available at update.json. The app checks it when opened,
using a six-hour cache; manual Settings checks bypass that cache. Updates never
silently replace the installed app. Finish or pause media downloads before installing.

## Publishing future updates

Prepare and test a new APK in the private development repository; increment its
version code and preserve the appropriate signing identity. Upload that APK,
matching source and checksums as a new release here. Publish update.json only after
verifying the assets. Preserve older releases.

A separate password-protected local admin panel is available to the project owner.
It verifies signed APKs, generates committed source snapshots, stages uploads,
checks remote hashes and publishes the feed last. It runs on the owner's laptop,
not in the Android app. Public updates remain hosted on GitHub when that laptop
is off. Admin credentials are not included in the APK or public source snapshots.

## Site support and optional analytics

StreamPocket uses the full yt-dlp site library and generic media detection, rather
than a YouTube-only host list. Website support varies; private, protected and live
videos are unsupported. Version 1.0.2 fixes direct audio links without a format ID.

Optional usage reporting is off by default and excludes video links, titles and
raw error messages. The owner's local admin can show GitHub APK download counts,
active reporting devices, device regions, versions and media/error counts. Device
region is not verified physical location. No public analytics hosting is configured;
local phone reporting requires USB forwarding. See ANALYTICS.md in the source ZIP.

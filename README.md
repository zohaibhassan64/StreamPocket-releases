# StreamPocket releases

Public downloads, release notes and released source snapshots for StreamPocket.
The ongoing development repository and its history are private. Source snapshots
of distributed versions are supplied here to recipients under the app's GPL-3.0
license; the private development repository is not needed to obtain those snapshots.

## Current status

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

## Two kinds of update

- The current app automatically checks for **yt-dlp engine** updates when used,
  at most once per day. This maintains the downloading engine.
- A **StreamPocket APK** update changes the app itself. Users currently download
  and install that APK from Releases. In-app APK update detection is not implemented.

Public update metadata will be made available at update.json after the release
assets have been uploaded and verified. This is preparation for a future APK
update checker; it does not modify already-installed APKs by itself.

## Publishing future updates

Prepare and test a new APK in the private development repository; increment its
version code and preserve the appropriate signing identity. Upload that APK,
matching source and checksums as a new release here. Publish update.json only after
verifying the assets. Preserve older releases.

A custom admin panel is not required to publish releases: GitHub's Releases page
can serve as the initial release-management interface. A later panel can provide
authenticated APK/source upload, release notes, review and publication. Its server
must hold publishing credentials; users' Android apps must never contain them.

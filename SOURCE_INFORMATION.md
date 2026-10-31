# Released source information

The StreamPocket application is GNU GPL-3.0. Each release provides an application
source snapshot and the license text alongside its APK. Recipients can obtain the
snapshot without access to private development history. The GPL permits recipients
to further share covered source; repository privacy is not a restriction on those
rights.

For the 1.0.0-test.1 APK:

- Application source snapshot: StreamPocket-1.0.0-test.1-source.zip.
  Source commit d754de4; application code is the same as tested commit e7b37f4;
  the later commit adds distribution documentation and Gradle launchers.
- Native wrapper source: youtubedl-android-0.18.1-source.zip.
  https://github.com/yausername/youtubedl-android/tree/0.18.1
  Repacked from that tag to exclude redundant compiled .so/.aar/.apk payloads and
  the wrapper's old executable yt-dlp zipapp. All Java/Kotlin code, Gradle build
  files, native build instructions and licenses are retained. The application
  build retrieves the pinned native artifacts through Maven; the matching engine
  source is supplied separately below.
- Download engine source: yt-dlp-2026.10.26-source.zip.
  https://github.com/yt-dlp/yt-dlp/tree/2026.10.26
- FFmpeg source: ffmpeg-7.1.1-source.zip from the official FFmpeg GitHub mirror.
  The arm64 libavutil binary's av_version_info value was inspected and identified
  as 7.1.1. This is the upstream source, not a claim that Termux-specific native
  packaging can be reproduced byte-for-byte from that archive alone.
- The source build uses Flutter 3.41.4 / Dart 3.11.1, Android SDK 36, Gradle 8.14,
  Android Gradle plugin 8.11.1 and the pinned Maven native artifacts listed in the
  application build file. Run flutter pub get before compiling.
- The wrapper includes prebuilt FFmpeg, Python and QuickJS native components.
  Its BUILD_FFMPEG.md and BUILD_PYTHON.md describe native package builds and upstream
  sources. Additional upstream information:
  https://ffmpeg.org/download.html
  https://github.com/termux/termux-packages
  https://github.com/python/cpython
  https://bellard.org/quickjs/
  GPL codec/filter dependencies enabled by the upstream FFmpeg build also have
  source available from their upstream projects and Termux package recipes:
  https://code.videolan.org/videolan/x264
  https://bitbucket.org/multicoreware/x265_git
  https://www.xvid.com/download/
  https://github.com/georgmartius/vid.stab
  https://github.com/breakfastquay/rubberband

The supplied archive is complete application source with its pinned dependency
definitions. It is not a claim of an independently verified, byte-for-byte rebuild
of every third-party prebuilt native library. Native upstream source/build details
and licenses remain applicable; see the included upstream wrapper source and
application THIRD_PARTY_NOTICES.md. Signing keys and credentials are excluded.

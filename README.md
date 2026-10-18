# Kung Fu Fighting APK reverse-engineering workspace

This repository is a separate workspace for authorized, local analysis of the supplied Kung Fu Fighting APK. It is intentionally separate from the Tesla project in `Tttt`.

## Current findings
- The supplied APK is a ZIP-based Android package using Unity Mono.
- The managed assembly is `assets/bin/Data/Managed/Assembly-CSharp.dll`.
- The embedded Unity version is reported as `4.6.1p5`.
- The target feature is a pre-fight character picker for Ninja, Samurai, and Monster.

## GitHub Actions analysis
Add the APK at `input/kung-fu-fighting.apk` (do not commit it publicly unless you have the right to redistribute it), then run **Actions → APK static inventory → Run workflow**. The workflow creates a downloadable analysis report. It does not modify or rebuild the APK.

## Honest status
No modified APK is currently built or runtime-tested. A playable character mod requires decoding Unity assets and decompiling the managed assembly, then repackaging/signing and testing on a device.

# YUNSH OS OpenHarmony

Independent OpenHarmony side branch for YUNSH OS on Raspberry Pi 5.

All Linux-based YUNSH OS releases are the mainline, including the current
`v3.1.6` release. This repository is a separate OpenHarmony release channel:
it has its own image, OTA manifest, version numbers, checksums and rollback
path. It does not replace or update any Linux mainline system.

## What is published here

This is a binary-release repository, not the complete source repository. It
publishes tested signed images, OTA packages and manifests, checksums, release
notes, feature descriptions and download/flash instructions. The proprietary
Pi 5 board port, drivers, pairing, permission bridge and other non-open
implementation details remain outside this repository.

## Product boundary

- OpenHarmony is the system layer; this is not a Debian image with a HAP copied
  into it.
- Android and Waydroid are intentionally not included.
- Applications use native OpenHarmony HAP packages.
- YUNSH liquid-glass surfaces, spatial windows, browser, Bluetooth motion
  tracking, Link, Orbit, input, gallery, recording, media and 5K display
  support are the target feature set and are released only as each area passes
  its applicable test gate.
- The visual language is YUNSH's own: bright optical-display surfaces,
  translucent hierarchy, direct manipulation, interruptible spring motion,
  reduced-motion and enhanced-contrast options. It is not an Apple clone and
  does not use private Apple protocols.

## First boot and OTA

The base image includes the boot firmware, drivers, OpenHarmony runtime and the
desktop needed to reach first use without GitHub. Optional extras may use a
network connection, but a failed download must not block the desktop.

Updates use only this repository's signed release manifest and OTA assets. They
never use any Linux mainline OTA channel. Do not install a mainline image or
OTA over this side branch.

## Status

No public image is declared usable until the native OpenHarmony build, clean
first boot and QEMU boot evidence have passed. Raspberry Pi 5 hardware, display,
Bluetooth, IMU and HAP installation claims require corresponding real-device
evidence and are listed separately in each release.

See the repository's Releases page for the current tested downloads.

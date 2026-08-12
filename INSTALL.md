# Download and install

## Before installing

1. Confirm that the release explicitly lists your Raspberry Pi 5 image.
2. Download the image, its `.sha256` file and the matching release notes.
3. Verify the checksum before writing any removable disk.
4. Use a spare SD card. Installing an image erases the selected card.

## Verify

```sh
shasum -a 256 -c YUNSH-OS-OpenHarmony-<version>.img.xz.sha256
```

## Flash

On macOS, decompress the verified image and write it to the selected SD card
with Raspberry Pi Imager or the release's supplied flash script. Check the
target disk identifier twice. Never select the Mac system disk.

## First boot

Connect the Pi 5 to the display, power and network only if optional online
components are needed. The base system and desktop must be able to start
without GitHub. Keep the first boot powered until the release notes say that
initial setup is complete.

## OTA

Use the updater built into the same side-branch release. It verifies the signed
manifest and package, stages the update atomically, keeps the previous slot for
rollback and reboots only after verification. Do not point the updater at the
mainline YUNSH OS release feed.

Hardware limits and known issues are release-specific; read them before
installing.

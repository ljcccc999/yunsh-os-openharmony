# Release checklist

- [ ] Native OpenHarmony product image built; no Debian rootfs used.
- [ ] Clean first boot reaches the desktop without GitHub.
- [ ] QEMU boot log archived; QEMU results are not called Pi 5 hardware proof.
- [ ] Pi 5 image layout, boot files and driver dependencies checked.
- [ ] HAP install/launch tested on a supported OpenHarmony target.
- [ ] OTA package and signed manifest verify successfully.
- [ ] OTA failure leaves the previous bootable slot intact.
- [ ] SHA-256 files generated for every published asset.
- [ ] Release notes list tested hardware and untested boundaries.
- [ ] No proprietary source, credentials, private protocol details or internal
      board-port files included in the public repository.

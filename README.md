# nvidia-390xx-linux-7.0

Testing repo for NVIDIA 390.157 on Linux 7.0.

Status: **build-only.** The AUR patch series applies and the modules build against 7.0 headers (tested on Ubuntu 7.0.0-38, gcc 15.2). The driver does not work: adapter init fails with `RmInitAdapter failed 0x12:0x45` and no GPU interrupts. Same result with Debian's 390 7.0 patches, with `pci=nomsi`, and with `NVreg_EnableMSI=0`.

For a working Fermi driver, stay on kernel 6.8.

Patches and hashes are in `patches/`, applied by `scripts/apply-aur-patches.sh`.

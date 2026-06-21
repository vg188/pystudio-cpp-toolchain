# PyStudio runtime packages

Source: `msmt2018/termux-packages`

This repository builds runtime packages for PyStudio:

- Android package: `com.vchangxiao.pystudio`
- Prefix: `/data/data/com.vchangxiao.pystudio/files/usr`
- Package format: Debian `.deb`

The default workflow builds `aarch64` packages for:

- `python`
- `python-pip`
- `nodejs`
- `npm`

Dependencies are built from source instead of downloaded from the official
Termux repositories, so the generated packages keep the PyStudio prefix.

The workflow publishes raw `.deb` files and a minimal apt repository archive
with `Packages`, `Packages.gz`, and `Packages.xz` indexes.

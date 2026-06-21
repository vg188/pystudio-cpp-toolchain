# PyStudio runtime packages

Source: `msmt2018/termux-packages`

This repository builds runtime packages for PyStudio:

- Android package: `com.vchangxiao.pystudio`
- Prefix: `/data/data/com.vchangxiao.pystudio/files/usr`
- Package format: Debian `.deb`

The default workflow builds `aarch64` packages for:

- `python`
- `python-pip`

Dependencies are built from source instead of downloaded from the official
Termux repositories, so the generated packages keep the PyStudio prefix.

The workflow publishes raw `.deb` files and a minimal apt repository archive
with `Packages`, `Packages.gz`, and `Packages.xz` indexes.

Additional packages such as `nodejs npm` can be built with `workflow_dispatch`
by passing them in the `packages` input.

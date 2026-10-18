# DNS-MITM Manager (fork)

Ultrahand (Tesla fork) overlay for Atmosphere's DNS MITM. Lets you toggle entries in the `hosts` files under `/atmosphere/hosts` and reloads them when the overlay is closed. Usage and file format are documented upstream: [ppkantorski/DNS-MITM_Manager](https://github.com/ppkantorski/DNS-MITM_Manager).

## Why this fork exists

This fork publishes a built overlay, kept current against libultrahand.

The overlay source is not modified.

## What differs from upstream

- CI builds the overlay with the Makefile and publishes a release.
- `libs/libultrahand` is a submodule. A daily job moves it to upstream's latest commit and cuts a release if it changed.
- The Makefile is adjusted for current libultrahand.
- devkitPro ships no minizip for the Switch, so CI builds it from zlib's source.

Release tags: `v*` for manual, `build-<date>-<libultrahand commit>` for automatic.

## Build

devkitPro (devkitA64, libnx), `switch-curl`, `switch-zlib`, `switch-mbedtls`, Switch minizip. Clone with `--recurse-submodules`, run `make`.

## Credits

[znxDomain](https://github.com/znxDomain/DNS-MITM_Manager) (original), [ppkantorski](https://github.com/ppkantorski) (libultrahand, [libultrahand](https://github.com/ppkantorski/libultrahand)), [WerWolv](https://github.com/WerWolv) (Tesla).

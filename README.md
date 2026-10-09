# M10_R01 Don't Be a Stock Blocker!

Neutralizes the vendor's hidden app-component blocklist.

A KernelSU Next module for the **Pritom Max 10 (M10_R01)**. Companion to the unlock/root guide:
[Pritom-Max-10-M10_R01-Unlock](https://github.com/thewickedlabs/Pritom-Max-10-M10_R01-Unlock).

The stock firmware ships `/vendor/etc/rockchip_forbid_packages.xml`, a hidden blocklist that quietly
disables specific components of certain apps **after you install them** — on this build: QQ
(`com.tencent.mobileqq`), AutoNavi Maps (`com.autonavi.minimap`) and Snaptube
(`com.snaptube.premium`). You never agreed to that; the vendor decided for you.

This module overlays that file with an **empty list**, so nothing is force-disabled and your apps run
as their makers intended. It's **systemless** — it mounts over the stock read-only `/vendor` file and
never writes to the partition. Disable the module and reboot, and the vendor blocklist is back.

## Requirements

- Pritom Max 10 (M10_R01)
- Rooted with KernelSU Next

The installer stops without changing anything if either is missing.

## Install

1. Download [`Pritom-Max-10-M10_R01-dbasb.zip`](https://github.com/thewickedlabs/Pritom-Max-10-M10_R01-dbasb/releases/latest/download/Pritom-Max-10-M10_R01-dbasb.zip) (latest release).
2. KernelSU Next → Modules → Install from storage → select the zip.
3. Reboot.

## Uninstall

Disable or remove the module and reboot. The vendor blocklist comes back untouched.

## License

[WTFPL](LICENSE). Use at your own risk; no warranty and no liability for anything this does to your device.

---

Wicked Labs · https://www.cyberspace7.org

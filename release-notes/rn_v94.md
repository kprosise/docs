# LmP V94 Release Notes

> [!NOTE]
  You can view the full [v94 changelog](https://foundries.io/products/releases/94/) for greater detail.

* [v94.1 Test Results](https://qa-reports.foundries.io/lmp/lmp-ci-testing/build/a045f38ac6fbd8e07fb6bd278163936e1de5b9b4/)
* [v94 Test Results](https://qa-reports.foundries.io/lmp/lmp-ci-testing/build/e27cb36c6c8df52df543887cdb6b407ce84ef33d/)

## Attention Points for Migration

Things to be aware of when [updating LmP](https://docs.foundries.io/94/reference-manual/linux/linux-update.html) from the v93 release:

> -   Base OE/Yocto version in v94.1 is still kirkstone (4.0.20)
> -   TI BSP updated to the 09.02.00.004 release, without major changes
> -   NVIDIA Tegra BSP updated to the L4T R35.5.0 release, without major changes
> -   NXP BSP updated to the lf-6.1.55-2.2.0 release, including updates to U-Boot
>     and Kernel, which could cause patch conflicts
> -   Go had a major update, from the 1.20.x series to the 1.22.5 release

Please also check the respective vendor BSP release notes for more
information.

## Known Issues

TODO: Update with post-release findings

## Aktualizr-Lite Updates

> -   Offline update bundles are now tied to a specific tag and device
>     type. This is enforced by a new signed metadata file added to the
>     bundle by fioctl >= 0.42
> -   Applications can be included in offline update bundles by using new
>     factory configuration parameters (containers.offline.enable and
>     containers.offline.app_shortlist), instead of having to enable image
>     preloading. See [Offline - Updates](https://docs.foundries.io/94/user-guide/offline-update/offline-update.html#prerequisites) for mode details
> -   Update events and callbacks are now enabled during offline updates
> -   Applications state verification, removal and pruning are now
>     performed by the composectl tool
> -   Fixes to check whether compose app images are installed and all its
>     containers are running in the following use cases: when one or more
>     app images are hosted in docker hub, more than one version of the
>     same app stored locally and when more than one app services/containers
>     are based on the same container image
> -   Bug fixes

## General Updates

### v94.1

> -   LMP release based on the OE/Yocto 4.0.20 Kirkstone release
> -   Boot firmware update support added for AM64XX
> -   Linux-lmp updated to the v6.1.102 stable release
> -   Linux-lmp-rt updated to the v6.1.102-rt37 stable release
> -   Linux-lmp-fslc updated to include the 6.1-2.2.0 tag
> -   Alsa sound support fixed for imx8m targets using the linux-lmp-fslc kernel

### v94

> -   LMP release based on the OE/Yocto 4.0.19 Kirkstone release
> -   Bitbake updated to the 2.0.19 release
> -   Linux-lmp updated to the v6.1.90 stable release
> -   Linux-lmp-rt updated to the v6.1.90-rt30 stable release
> -   Linux-lmp-ti-staging updated to the 09.02.00.004 tag
> -   Go updated to the 1.22.5 stable release
> -   Rust updated to the 1.75 stable release
> -   OpenSSL updated to the 3.0.14 stable release
> -   Linux-firmware updated to the 20240220 snapshot
> -   TI BSP updated to the 09.02.00.004 release
> -   NXP BSP updated to the lf-6.1.55-2.2.0 release
> -   NVIDIA Tegra BSP updated to the L4T R35.5.0 release

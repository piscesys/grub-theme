# Piscesys-grub-theme
The default GRUB theme for Pisces System. A fork from [gustawho](https://github.com/gustawho/grub2-theme-breeze)

## License
GPLv3, which CC BY-SA, the license for grub2-theme-breeze, is one-way compatible with.

## Installation
On Debian or Debian-based distros you can simply install the Debian package in the release.

For non-Debian-based distros, copy the "piscesys" directory to `/usr/share/grub/themes/`, and "piscesys.cfg" to `/etc/default/grub.d/`.

And then run:

`sudo update-grub`

## Build Debian package

```shell
sudo mk-build-deps ./debian/control -i -t "apt-get --yes" -r
dpkg-buildpackage -b -uc -us
```
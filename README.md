# Piscesys-grub2-theme
The default GRUB2 theme for Pisces System. A fork from [gustawho](https://github.com/gustawho/grub2-theme-breeze)

## License
GPLv3, which CC BY-SA, the license for grub2-theme-breeze, is one-way compatible with.

## Installation
On Debian or Debian-based distros you can simply install the Debian package in the release.

For non-Debian-based distros, copy the "piscesys" directory to a location GRUB can access it. The standard path is `/usr/share/grub/themes/`, but if your installing this theme in an encrypted system, you might prefer to copy this package content to `/boot` and set your GRUB configuration file accordingly.

Edit `/etc/default/grub`, making sure this line (or a variant of it) exists:

`GRUB_THEME="/usr/share/grub/themes/piscesys/theme.txt"`

And then run:

`sudo grub-mkconfig -o /boot/grub/grub.cfg`

## Build Debian package

```shell
sudo mk-build-deps ./debian/control -i -t "apt-get --yes" -r
dpkg-buildpackage -b -uc -us
```
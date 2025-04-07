This repo has been reconstructed from [this](https://web.archive.org/web/20241208143553/https://github.com/lucy/tewi-font) archive.org snapshot. Everything is the same as the original except for this line in the README and the screenshots folder, which was hosted elsewhere in the original repo. Every file in variant and scripts (except for `tewi2a-medium-11.bdf`) is missing. Please make pull request if you have them.

![](screenshots/screenshot1.png)

#### tewi-medium

![](screenshots/screenshot2.png)

#### tewii-medium

![](screenshots/screenshot3.png)

#### tewi2a-medium

![](screenshots/screenshot4.png)

#### tewi-bold

![](screenshots/screenshot5.png)

#### tewii-bold

![](screenshots/screenshot6.png)

#### tewi2a-bold

![](screenshots/screenshot7.png)


## Building

#### Requirements

* python 3 (variant generator)
* bdftopcf (.pcf files)

Run `make` to build PCFs. To only build the standalone BDF files run `make var`.

## Installing

#### Arch

[AUR Package](https://aur.archlinux.org/packages/bdf-tewi-git/)

#### Crux

[6c37/pcf-tewi](https://web.archive.org/web/20241008052457mp_/https://github.com/6c37/crux-ports)

#### X11

```sh
$ make fontdir
$ xset +fp /path/to/tewi-font/out # you should do this every time X starts
                                  # e.g. put it in your ~/.xinitrc
```

#### Fontconfig

```sh
$ make
$ ln -s /path/to/tewi-font/out ~/.fonts/tewi
$ fc-cache -fv
```

NOTE: If your distro has a file like `70-no-bitmaps.conf` in `/etc/fonts/conf.d`, and tewi doesn't work, you should remove it.

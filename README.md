<p align=center>
<br>
<a href="http://makeapullrequest.com"><img src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg"></a>
<img src="https://img.shields.io/badge/os-linux-brightgreen">
<img src="https://img.shields.io/badge/os-android-brightgreen"></a>
<br>
<a href="https://github.com/CoolnsX"><img src="https://img.shields.io/badge/maintainer-CoolnsX-blue"></a>
<a href="https://github.com/iamchokerman"><img src="https://img.shields.io/badge/maintainer-iamchokerman-blue"></a>

</p>

A command line interface to browse and watch Korean Drama or watch Chinese drama. This tool scrapes the site [draplay](https://draplay.io).

This tool is modified version of [ani-cli](https://github.com/pystardust/ani-cli) by pystardust which is anime scraping tool and updated version of [dra-cla](https://github.com/CoolnsX/dra-cla) by CoolnsX.

## Table of Contents
- [Install](#Installation)
  - [Linux](#Linux)
    - [Nix](#Nix)
  - [Android](#Android)
- [Uninstall](#Uninstall)
- [Dependencies](#Dependencies)
- [Disclaimer](./disclaimer.md)

## Install

### Linux

Install dependencies [(See below)](#Dependencies)

## Dependencies

- grep
- sed
- curl
- openssl
- mpv - Video Player
- aria2 - Download manager
- ffmpeg - m3u8 Downloader

```sh
git clone https://github.com/iamgalenc/dra-cla && cd dra-cla
sudo cp dra-cla /usr/local/bin/dra-cla
```

*Note that mpv installed through flatpak is not compatible*

#### Nix

``` shell
nix-shell -p dra-cla
```

### Android

Install termux [(Guide)](https://termux.com/)

```sh
pkg update
pkg install git termux-tools ncurses-utils openssl-tool ffmpeg -y
git clone https://github.com/CoolnsX/dra-cla && cd dra-cla
cp dra-cla $PREFIX/bin/dra-cla
echo 'am start -n is.xyz.mpv/.MPVActivity "$1"' > $PREFIX/bin/mpv
chmod +x $PREFIX/bin/mpv
```

Install mpv-android [(Link)](https://play.google.com/store/apps/details?id=is.xyz.mpv)

*Add ```referrer="https://asianembed.io"``` to mpv.conf (Open mpv app, goto three dots top right->Settings->Advanced-->Edit mpv.conf)* 

*Note: VLC android doesn't support referrer option. So it will not work*

## Uninstall

* Linux: ```sudo rm /usr/local/bin/dra-cla```
* Android: ```rm $PREFIX/bin/dra-cla```

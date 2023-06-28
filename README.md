# Age of Empires Online - (Project Celeste) Lutris install script

>  Lutris script to install Project Celeste (Age of Empires Online)

Please note the installer files are temporarily unavailable, will be restored asap!

## Table of contents
* [General info](#general-info)
* [Requirements](#requirements)
* [Setup](#setup)
* [Update](#updating-the-game)
* [Language](#change-the-language-of-the-game)
* [Tweaks](#tweaks)
* [Issues](#issues)
* [Links](#links)

## General info
Age of Empires Online was revived in mid-2017 under a non-commercial license under Microsoft's "Game Content Usage Rules" by an independent group of developers (Project Celeste). It can be played on a community-run server known as "Project Celeste" with all online features fully enabled, for free without any player limitations!
The team uses Microsoft's publicly released development-kit to balance, fix bugs, and expand the content where Microsoft's team left off.

This script brings the game to Linux users aswell, it makes the install easy!

<img width="964" alt="AOEO Example Lutris" src="https://github.com/Toetje585/Age-of-Empires-Online-Lutris/blob/master/age-of-empires-online.png">


## Requirements

**Distro:**

Tested on Ubuntu 20.04/10 and Arch Linux however all distro's that run [Lutris](https://lutris.net/downloads/) should be supported.

**GPU + Driver that supports Vulkan:**

Ubuntu: For the best performance on Nvidia, it is recommended to switch to the latest proprietary driver in Software-Properties > Additional Drivers. If on AMD or Intel, it is recommended to install `mesa-vulkan-drivers:amd64` and `mesa-vulkan-drivers:i386`

Arch: For Nvidia users, install `nvidia` or `nvidia-lts` and their lib32 counterparts if you use `linux` or `linux-lts` respectively. If on AMD or Intel, install `mesa` and its lib32 counterparts, as well as `vulkan-radeon` or `vulkan-intel`, depending on GPU vendor.

**Packages:**

| Ubuntu 20.10  |  Ubuntu 20.04 | Arch |
| ------------- | ------------- | ---- |
| gstreamer1.0-plugins-good:i386  | gstreamer1.0-plugins-good:i386  | lib32-gst-plugins-good |
| gstreamer1.0-plugins-good:amd64  | gstreamer1.0-plugins-good:amd64  | gst-plugins-good |
| winehq-stable:amd64 | winehq-stable:amd64 | wine-stable |
| winehq-stable:i386 | winehq-stable:i386 | wine-stable |

Tip: If on Debian or derivative, use ```--install-recommends``` once installing wine and or Lutris. Ubuntu users can enable 32bit packages beforehand using ```sudo dpkg --add-architecture i386 && sudo apt update```. Lutris allows you to switch to staging and or devel wine builds, so installing winehq-staging/winehq-devel 32bit and amd64 packages could give you the latest experimental wine runtimes.

## Setup

Download the script and start the installation by using:
```
$ lutris -i ~/path_to_script/age-of-empires-online.yaml
```

## Updating the game

## Change the language of the game

## Tweaks

## Issues

## Links

[Celeste Website](https://www.projectceleste.com/)<br/>
[Celeste Github](https://github.com/ProjectCeleste/)<br/>
[Lutris](https://lutris.net/games/age-of-empires-online/)<br/>

Script created by [@Toetje583] game and launcher maintained by the amazing Project Celeste team!

# Age of Empires Online - (Project Celeste) Lutris install script

>  Lutris script to install Project Celeste (Age of Empires Online)

## Table of contents
* [General info](#general-info)
* [Requirements](#requirements)
* [Ubuntu 26.04](#ubuntu-2604)
* [Setup](#setup)
* [Post Install](#post-install)
* [Update](#updating-the-game)
* [Language](#change-the-language-of-the-game)
* [Notes](#notes)
* [Issues](#issues)
* [Links](#links)

## General info
Age of Empires Online was revived in mid-2017 under a non-commercial license under Microsoft's "Game Content Usage Rules" by an independent group of developers (Project Celeste). It can be played on a community-run server known as "Project Celeste" with all online features fully enabled, for free without any player limitations!
The team uses Microsoft's publicly released development-kit to balance, fix bugs, and expand the content where Microsoft's team left off.

This script brings the game to Linux users aswell, it makes the install easy!

Tested successfully again on 07-07-2026.

Important: use the regular system Wine version for this script. Proton-based Wine builds and other custom Wine builds might work, but have caused issues before, while regular Wine has been consistently stable.

<img width="964" alt="AOEO Example Lutris" src="https://github.com/Toetje585/Age-of-Empires-Online-Lutris/blob/master/age-of-empires-online.png">


## Requirements

**Distro:**

Tested on Ubuntu 20.04/10, Arch Linux, and CachyOS, however all distro's that run [Lutris](https://lutris.net/downloads/) should be supported.

On CachyOS, only the gaming package needs to be enabled:
https://wiki.cachyos.org/configuration/gaming/

**GPU + Driver that supports Vulkan:**

Ubuntu: For the best performance on Nvidia, it is recommended to switch to the latest proprietary driver in Software-Properties > Additional Drivers. If on AMD or Intel, it is recommended to install `mesa-vulkan-drivers:amd64` and `mesa-vulkan-drivers:i386`

Arch: For Nvidia users, install `nvidia` or `nvidia-lts` and their lib32 counterparts if you use `linux` or `linux-lts` respectively. If on AMD or Intel, install `mesa` and its lib32 counterparts, as well as `vulkan-radeon` or `vulkan-intel`, depending on GPU vendor.

**Packages:**

Tip: If on Debian or derivative, use ```--install-recommends``` once installing wine and or Lutris. Ubuntu users can enable 32bit packages beforehand using ```sudo dpkg --add-architecture i386 && sudo apt update```. For this game, prefer regular system Wine over Proton-based or other custom Wine builds.

For all distro's see this [link](https://www.gloriouseggroll.tv/how-to-get-out-of-wine-dependency-hell/)

## Ubuntu 26.04

To use this script on Ubuntu 26.04, these steps should be enough:

1. Enable 32-bit support and update package metadata:
```
sudo dpkg --add-architecture i386
sudo apt update
```

2. Install Lutris and common Wine/Lutris dependencies:
```
sudo apt install --install-recommends lutris winetricks mesa-vulkan-drivers mesa-vulkan-drivers:i386
```

3. If the Ubuntu repo version of Lutris is missing or too old, install the latest `.deb` from Lutris releases:
https://github.com/lutris/lutris/releases

4. Install this script as usual:
```
lutris -i ~/path_to_script/age-of-empires-online.yaml
```

5. Use the regular system Wine version for the game. Avoid Proton-based Wine builds and other custom Wine builds for this title, as they can work but have caused issues in the past.

## Setup

Download the script and start the installation by using:
```
$ lutris -i ~/path_to_script/age-of-empires-online.yaml
```

During installation, you might see warnings about the 64-bit Wine prefix. Those warnings can be ignored.

## Post Install

After the game is installed in Lutris:

1. Start the Project Celeste launcher.
2. Log in with your account.
3. Run a **Game Scan** first before starting the game.

Permanent co-op fix reported by [robertknexen](https://forums.projectceleste.com/members/robertknexen.6687/):

```
echo "net.ipv4.ip_unprivileged_port_start=1000" | sudo tee /etc/sysctl.d/99-aoeo-coop.conf
```

## Updating the game

Running a **Game Scan** in the launcher should do the job.

## Change the language of the game

The game language can be changed from within the launcher.

## Notes

On first start, the game resolution might be incorrect. Set it to your monitor's correct resolution and the game should switch to fullscreen properly.

## Issues

If the .NET Framework installation fails inside the Wine prefix, you may not be able to launch missions and can get a map loading error.

## Links

[Celeste Website](https://www.projectceleste.com/)<br/>
[Celeste Github](https://github.com/ProjectCeleste/)<br/>
[Lutris](https://lutris.net/games/age-of-empires-online/)<br/>

Script created by [@Toetje583] game and launcher maintained by the amazing Project Celeste team!

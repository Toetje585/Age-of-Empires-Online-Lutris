# Age of Empires Online - (Project Celeste) Lutris install script

>  Lutris script to install Project Celeste (Age of Empires Online)

## Table of contents
* [General info](#general-info)
* [Requirements](#Requirements)
* [Setup](#setup)
* [Update](#Updating-the-game)
* [Language](#Change-the-language-of-the-game)
* [Features](#features)
* [Issues](#issues)
* [Status](#status)
* [Links](#links)

## General info
Age of Empires Online has been revived in mid-2017 under a non-commercial license under Microsoft's "Game Content Usage Rules" by an independent group of developers (Project Celeste). It can be played on a server emulator known as "Project Celeste" with all online features fully enabled, for free without any player limitations!
The team uses Microsoft's publicly released development-kit to balance, fix bugs, and expand the content where Microsoft's team left off.

This script brings the game to Linux users aswell, it makes the install easy but if you do not preffer to use Lutris the install script is able to point you what you would need in a wineprefix.

<img width="964" alt="AOEO Example Lutris" src="https://github.com/Toetje585/Age-of-Empires-Online-Lutris/blob/master/age-of-empires-online.png">


## Requirements

**Distro:**

Tested on Ubuntu 20.04/10 however all distro's hat run [Lutris](https://lutris.net/downloads/) should be supported.

**GPU + Driver that supports Vulkan:**

For the best perfromance open the Software & Updates application window. Select TAB Additional Drivers and choose any proprietary NVIDIA/AMD driver. The higher the driver number the latest the version. Alternatively users can download the latest drivers from NVIDIA/AMD directly, please reffer to guides on how to install them.

**.Net Core 3.1 SDK:**

For any other not based distro on debian you need to enable the i386 architecture, please reffer to distro instructions on how to enable them.
It's recommended to install winehq-stable, winehq-staging and or winehq-devel to the system according to distro guidelines. Also make sure the distro is able to make use of .NET Core 3.1 SDK.

**Packages:**

| Ubuntu 20.10  |  Ubuntu 20.04 |
| ------------- | ------------- |
| gstreamer1.0-plugins-good:i386  | gstreamer1.0-plugins-good:i386  |
| gstreamer1.0-plugins-good:amd64  | gstreamer1.0-plugins-good:amd64  |
| winehq-stable:amd64 | winehq-stable:amd64 |
| winehq-stable:i386 | winehq-stable:i386 |

Tip: use ```--install-recommends``` once installing wine and or Lutris. Ubuntu users can enable 32bit packages beforehand using ```sudo dpkg --add-architecture i386 && sudo apt update```. Lutris allows you to switch to staging and or devel wine builds, so installing winehq-staging/winehq-devel 32bit and amd64 packages could give you the latest experimental wine runtimes.

## Setup

Download the script and start the installation by using:
```
$ lutris -i ~/path_to_script/age-of-empires-online.yaml
```

After install make sure to set the correct account details:

<img width="964" alt="Set Account Details" src="https://github.com/Toetje585/Age-of-Empires-Online-Lutris/blob/master/setaccount.png">


## Updating the game

Install .NET Core 3.1 SDK according to [Microsoft Documentation](https://docs.microsoft.com/en-us/dotnet/core/install/linux-ubuntu)<br/>

```
$ git clone https://github.com/ProjectCeleste/Celeste.GameScan.git
$ cd Celeste.GameScan && dotnet build
$ cd bin/Debug/netcoreapp3.1
$ ./Celeste.GameScan --verbose-mode --game-dir "/home/username/Games/age-of-empires-online/drive_c/Program Files/Age Of Empires Online/"
```
## Change the language of the game
Use this startup parameter to change the language, args: --email "" --password "" **--ignore_rest LauncherLang="de-DE"**

**Supported language values:**

"de-DE"
"en-US"
"es-ES"
"fr-FR"
"it-IT"
"zh-CHT"
"pt-BR"

## Features
List of features ready and TODOs for future development
* Updating the game trough CLI (https://github.com/ProjectCeleste/Celeste.GameScan) 
* ...
* ...

To-do list:
* Finalyzing the installer script
* Account creation

## Issues

* Co-op play only works if wine has access to privileged ports using setcap (Asked celeste dev's to leave the privileged ports range)

## Status
Project is: in development

## Links

[Celeste Website](https://www.projectceleste.com/)<br/>
[Celeste Github](https://github.com/ProjectCeleste/)<br/>
[Lutris](https://lutris.net/games/age-of-empires-online/)<br/>

Script created by [@Toetje583] game and launcher mainainted by the amazing Project Celeste team!

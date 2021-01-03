# Age of Empires Online - (Project Celeste) Lutris install script.

>  Lutris script to install Project Celeste (Age of Empires Online)

## Table of contents
* [General info](#general-info)
* [Requirements](#Requirements)
* [Setup](#setup)
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

For any other not based on debian you need to enable the i386 architecture, please reffer to distro instructions on how to enable them.
It's recommended to install winehq-stable, winehq-staging and or winehq-devel to the system according to distro guidelines.

## Setup

Download the script and start the installation by using:
```
$ lutris -i ~/path_to_script/age-of-empires-online.yaml
```
## Features
List of features ready and TODOs for future development
* Updating the game trough CLI (https://github.com/ProjectCeleste/Celeste.GameScan)
* ...
* ...

To-do list:
* Finalyzing the installer script
* Account creation

## Issues

* Co-op play only works if wine has acces to privileged ports using setcap

## Status
Project is: in development

## Links

[Celeste Website](https://www.projectceleste.com/)<br/>
[Celeste Github](https://github.com/ProjectCeleste/)<br/>
[Lutris](https://lutris.net/games/age-of-empires-online/)<br/>

Script created by [@Toetje583] game and launcher mainainted by the amazing Project Celeste team!

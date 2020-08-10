# RetroArch & libRetro for KISSLinux

:construction: This is a WIP on how to setup `retroarch` and friends.
:construction:

## Install

```
~ $ git clone https://github.com/sdsddsd1/kiss-games
~ $ export KISS_PATH=$KISS_PATH:$HOME/kiss-games/equipment
~ $ export KISS_PATH=$KISS_PATH:$HOME/kiss-games/libretro
~ $ kiss b retroarch
~ $ kiss i retroarch
```

The emulators, so called 'cores', start with `libretro-` followed by the
corresponding name, can be installed with the following:

```
~ $ kiss b libretro-$core
~ $ kiss i libretro-$core
```

Once installed, retroarch will pick them up.

## Usage

In order to change configuration, that can be found, and edited in:
```
~ $ vi $HOME/retroarch/retroarch.cfg
```
Firmware goes inside:
```
~ $ $HOME/.config/retroarch/system/
```
And roms have no specified path and can live anywhere on the system. They are added
inside retroarch menu.

 * 'Import content -> Scan directory'

Furthermore, if someone needs more complete documentation can be found [here](https://docs.libretro.com).

## KISS way

The online updater is disabled as retroarch's buildsystem is targeted at `glibc`
and therefore the whole suite is managed by the package manager. Only preview
thumbnails are downloaded once at runtime.

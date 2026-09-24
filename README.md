# Qualyx

Qualyx runs *Half-Life: Alyx* natively on standalone Meta Quest headsets. Builds
are published on the [Releases](../../releases) page.

Join our community on [Discord](https://discord.gg/E5VVNyQQX4) for support and discussion.

Qualyx is experimental. It is developed and tested on Quest 3; Quest 2 support
is less tested and uses reduced graphics settings.

The release does not include Valve's game files. You need your own Steam copy
of *Half-Life: Alyx*.

## Requirements

- A Meta Quest headset with Developer Mode enabled.
- *Half-Life: Alyx* on Steam.
- Enough free headset storage for the APK and your game files.

## Install or update

Download the latest APK from the [Releases](../../releases/latest) page and
install it with SideQuest, adb, or another APK sideloading tool. With adb:

```sh
adb install -r Qualyx-<version>.apk
```

Use `-r` when updating so Android keeps the app's existing data and settings.

## Add the game files

You only need the `hlvr` and `core` folders inside your *Half-Life: Alyx*
`game` folder. Copy those two folders to `/sdcard/Qualyx/game` on the headset.
You can copy the entire `game` folder instead if you prefer; the other folders
are not required by Qualyx. The result should include these files:

```text
/sdcard/Qualyx/game/hlvr/pak01_dir.vpk
/sdcard/Qualyx/game/core/pak01_dir.vpk
```

You can copy the folders with SideQuest, MTP, or adb. For example:

```sh
adb shell mkdir -p /sdcard/Qualyx/game
adb push "/path/to/Half-Life Alyx/game/hlvr" /sdcard/Qualyx/game/
adb push "/path/to/Half-Life Alyx/game/core" /sdcard/Qualyx/game/
```

To copy the entire `game` folder instead:

```sh
adb push "/path/to/Half-Life Alyx/game/." /sdcard/Qualyx/game/
```

### Older 1.5.4 game files

If you have the older May 2022 version 1.5.4 game files, download
[`Qualyx-2022-shaders.zip`](https://drive.google.com/file/d/17M6ZWhhGb0UnLdv7e5hJ1CmUz_pAsazD/view?usp=sharing)
to the headset. In Qualyx, choose your game folder, select **Import 2022 shader
pack**, and choose that ZIP file. Keep Qualyx open while it imports and verifies
the shaders.

If you have the newest game files, this step is not needed.

Open Qualyx from **Library → Unknown Sources**, allow file access, choose the
game folder if it is not detected automatically, and select **Launch in VR**.

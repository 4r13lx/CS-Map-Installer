# CS-Map-Installer
Counter-Strike map installer developed in bash during this damned COVID-19 pandemic.

## Description
This script helps you to copy or upload map files directly into game folder. It has many features such as:

- Find and validate game and fastDL folders (Locally or remotely) automatically
- Check integrity and uncompress ZIP and RAR files directly
- Copy files to local or remote (via SSH/SCP) game folder
- Compress map files into bz2 archive
- Upload bz2 file to the local or remote fastDL server

## Install
As you know, download and copy it into your maps folder. What map folder? The map folder that you previously created to download and store all maps downloaded from any cs maps page.
I highly recommend to you to leave this script into the map folder because sometimes, depends on GNU/Linux distribution, do not recongnize the paths when you pass them by argument.

## Usage
Try the following execution methods (Could be possible you need to use 'sudo' elevate permissions to hold temp files into '/tmp' system folder):
Use "./" or "sh" command to execute it.

```
1) sh css_MapInstaller -g [GAME_PATH] -m [MAP_PATH]    - Copy local files
2) sh css_MapInstaller -v -g [GAME_PATH] -m [MAP_PATH] - Shows detailed information (Verbose activated)
3) sh css_MapInstaller -v -u -m [MAP_PATH]             - Use default paths and shows detailed information (Verbose activated and using default paths)
```

The following libraries will be installed automatically in case of your system does not have them:
- unzip
- unrar
- sshpass
- bzip2

## Commands
```
-h         Display help
-g         Set game path in which reside folders such as 'maps', 'materials', 'sound', etc.
-m         Set map path in which reside map file downloaded (compressed)
-f         Set fast downloader map path to allocate compressed file
-r         Set remote game server to transfer files via SCP (eg.: username@server.domain:port)
-d         Set remote fastdl server to transfer files via SCP (eg.: username@server.domain:port)
-u         Unset game, fastdl and remote parameters to use default paths (You can edit this script to set your own paths)
           GAME_PATH="/home/user/cstrike"
           FASTDL_PATH="/var/www/html/css/maps"
           GAME_REMOTE_SERVER="user@servername:port"
           FASTDL_REMOTE_SERVER="user@servername:port"
-v         Set verbose information enabled. If you want to use it, must be the first command. (Do you really wanna see all the process details?)
```

## Compatibility
This script is compatible with CS 1.6, CS: Condition Zero and CS: Source.

## Special thanks
* Thanks to Gonza (@Mirko) to provide servers and his life-time to test this script.
* And many thanks to my brother/friends to back to the past enjoying this wonderful game with a 🍺 at my side!

---
⌨️ with ❤️ by [4r13lx](https://github.com/4r13lx) or @JasonBourne (CS nickname) 😊

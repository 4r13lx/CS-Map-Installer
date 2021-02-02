# CS-Map-Installer
Counter-Strike map installer developed in bash

# Description
This script helps you to copy or upload map files directly into game folder. It has manu features such as:

1- Validate game and fastDL folders (Locally or remotely)
2- Check integrity and uncompress ZIP and RAR files directly
3- Copy files to the local or remote (via SSH/SCP) game folder
4- Compress map files into bz2 archive
5- Upload bz2 file to the local or remote fastDL server

# Usage
Try the following execution methods (Could be possible you need to use sudo elevate permissions to hold temps file into '/tmp' system folder):
Use "./" or "sh" command to execute it.
1) sh css_MapInstaller -g [GAME_PATH] -m [MAP_PATH] 	  - Copy local files
2) sh css_MapInstaller -v -g [GAME_PATH] -m [MAP_PATH]  - Shows detailed information (Verbose activated)
3) sh css_MapInstaller -v -u -m [MAP_PATH] 			        - Use default paths and shows detailed information (Verbose activated and using default paths)

The following libraries will be installed automatically in case of your system does not have them:
- unzip
- unrar
- sshpass
- bzip2

# Commands
-h         Display help
-g         Set game path in which reside folders such as 'maps', 'materials', 'sound', etc.
-m         Set map path in which reside map file downloaded (compressed)
-f         Set fast downloader map path to allocate compressed file
-r         Set remote game server to transfer files via SCP (eg.: username@server.domain:port)
-d         Set remote fastdl server to transfer files via SCP (eg.: username@server.domain:port)
-u         Unset game, fastdl and remote parameters to use default paths (You can edit this script to set your own paths)
           GAME_PATH="/home/user/cstrike/maps"
           FASTDL_PATH="/var/www/html/css/maps"
           GAME_REMOTE_SERVER="user@servername:port"
           FASTDL_REMOTE_SERVER="user@servername:port"
-v		   Set verbose information enabled. If you want to use it, must be the first command. (Do you really wanna see all the process details?)

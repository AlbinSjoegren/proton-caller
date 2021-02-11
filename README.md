# Proton-Caller
Run any Windows program through [Valve's Proton](https://github.com/ValveSoftware/Proton).

[Usage](https://github.com/caverym/Proton-Caller#usage)

Please create an issue if you want added features or have an issue.

https://aur.archlinux.org/packages/proton-caller/

## Problem Reporting:
Please create an issue on the [Github](https://github.com/caverym/Proton-Caller) page which lists: system, kernel version, game, shell, and if it is or isn't a Steam game – provide how you had installed it and where it is installed. Additionally provide screenshots of the shell. Try many methods to get it to work and describe what you did in your issue.


## Usage:

```
Usage: proton-all VERSION PROGRAM
   or: basename OPTION PATH PROGRAM
Execute PROGRAM with Proton VERSION
If specified, run proton PATH

  -c, --custom PATH   use proton from PATH
  --help              display this help message
  --version           display version information
```

```
proton-call 5.13 SpaceEngine.exe
```

```
proton-call -c "/home/avery/.steam/steam/steamapps/common/Proton 5.13" SpaceEngine.exe
```
## Install:

To install `proton-call`
```
yay -S proton-caller
 ``` 

or: (with makepkg)

```
git clone https://aur.archlinux.org/proton-caller.git
cd proton-caller
makepkg -si
```
or:
```
git clone https://github.com/caverym/Proton-Caller.git
cd Proton-Caller
sudo cargo install --path .
```

### Space Engine example:
   Make a .desktop launcher. [example file](Space%20Engine.desktop)
   
   ```
[Desktop Entry]
Type=Application
Name=Space Engine
Comment=Space Engine
Exec=proton-call 5.13 SpaceEngine.exe
Path=/home/avery/Documents/games/SpaceEngine/system
Terminal=false
StartupNotify=false
   ```

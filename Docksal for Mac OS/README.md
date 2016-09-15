# Docksal for Mac OS Installer

## System Requirements

[Packages](http://s.sudre.free.fr/Software/Packages/about.html)

## Building new version

1. Put new versions of `docker*` binaries into `payload` folder
2. Download VirtualBox version that is supported by latest boot2docker and extract VirtualBox.pkg into `payload` folder
3. Change VirtualBox version in [payload/VirtualBox.VERSION.txt](payload/VirtualBox.VERSION.txt)
4. Change VirtualBox version in Project > Presentation > VirtualBox in Packages project and save it.
5. `/usr/local/bin/packagesbuild -v "Docksal for Mac OS.pkgproj"`
6. Build result is in `build` folder
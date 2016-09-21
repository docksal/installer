# Docksal for Mac OS Installer

## System Requirements

1. [Packages](http://s.sudre.free.fr/Software/Packages/about.html)
2. npm install -g appdmg (https://github.com/LinusU/node-appdmg)

## Files

`build` - target dir for PKG build  
`dmg/dmg.json` - dmg file description for appdmg util to generate DMG  
`payload` - files to be packed into PKG to be deployed onto user Mac  
`script` - internal PKG scripts  
`texts` - PKG texts  
`Docksal for Mac OS.pkgproj` - Packages project to create PKG installer

## Building new version

1. Put new versions of `docker*` binaries into `payload` folder
2. Download VirtualBox version that is supported by latest boot2docker and extract VirtualBox.pkg into `payload` folder
3. Change VirtualBox version in [payload/VirtualBox.VERSION.txt](payload/VirtualBox.VERSION.txt)
4. Change VirtualBox version in Project > Presentation > VirtualBox in Packages project and save it.
5. `/usr/local/bin/packagesbuild -v "Docksal for Mac OS.pkgproj"`

Installer is ready. Now packing it into dmg:

6. `mv "build/Docksal for Mac OS.pkg" dmg/`
7. `cd dmg && appdmg dmg.json "Docksal for Mac OS.dmg"`
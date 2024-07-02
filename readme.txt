uxn for macOS

provides:
 - resize with arbitrary scale while retaining fixed ratio
 - remove black padding border
 - no titlebar or traffic light buttons (just use shortcuts)
 - nice icon by rek that you can embed into the emulator

somehow retains topbar functionality while allowing drag

apply patch on the sdl2 branch of the sdl repo (https://github.com/libsdl-org/SDL/tree/SDL2)
and the uxn sdl2 emulator on sourcehut (https://git.sr.ht/~rabbits/uxn)

uxnemu has an ugly exec script icon in the dock when launching, but using *magic* and 
weird carbon era logic, you can use the extended attributes of the macOS filesystems, HFS+ and APFS 
to add a beautiful icon. unfortunately git cannot comprehend such dark arts (email linus)

use https://github.com/mklement0/fileicon (brew install fileicon) and then 
`fileicon set /usr/local/bin/uxnemu icon.png` (the png from this repo)

what's left:
 - doing some logic to embed the roms into the binary for easy distribution
    (probably using xxd -i and convoluted C logic)
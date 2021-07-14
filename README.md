# xscreensaver Settings

A cheatsheet for my preferred xscreensaver settings.

## Table of Contents:

* [Display Modes](https://github.com/yesmaybenookay/xscreensaver-settings#display-modes)
* [Advanced Settings](https://github.com/yesmaybenookay/xscreensaver-settings#advanced-settings)
* [Enabled Screensavers](https://github.com/yesmaybenookay/xscreensaver-settings#enabled-screensavers)
* [Screensaver  Specific Advanced Settings](https://github.com/yesmaybenookay/xscreensaver-settings#screensaver-specific-advanced-settings)
    * [Apple 2](https://github.com/yesmaybenookay/xscreensaver-settings#apple-2-settings)
    * [maze3d](https://github.com/yesmaybenookay/xscreensaver-settings#maze3d-settings)
    * [Phosphor](https://github.com/yesmaybenookay/xscreensaver-settings#phosphor-settings)

## Display Modes:

* Mode: Random Screensaver
* Blank After: 5 minutes
* Cycle After: 5 minutes
* Lock Screen After: disabled

## Advanced Settings:

### Image Manipulation:

* Grab Desktop Images - *This setting gives screensavers which manipulate images a cool effect.*

### Text Manipulation

* Text File - `/PATH/TO/TEXTFILE.txt`

OR

* Program - `fortune` or `fortune -s`

## Enabled Screensavers:

* Apple 2
* BSOD - *Enabled: (MS-DOS, OS/2, OS/390, HVX/GCOS, Encom, DVD, VMS, BSD, Linux (fsck), Linux (sparc), Linux (hppa), SCO, HPUX)*
* Circuit - disabled
* Decay Screen - disabled
* Distort - disabled
* Flip Screen 3D - disabled
* Flying Toasters
* GFlux - disabled
* GL Matrix
* Gravity Well
* Handsy
* Headroom
* Juggler 3D
* m6502
* Maze 3D
* Mem Scroller
* Molecule
* Peepers
* Penetrate
* Phosphor
* Pong
* Providence
* Scooter
* Slide Screen - disabled
* Slip - disabled
* Spotlight - disabled
* Time Tunnel
* Unknown Pleasures
* Vigilance - disabled
* XAnalogTV - disabled
* XFlame
* XMatrix

## Screensaver Specific Advanced Settings:

### Apple 2 Settings:

#### Default:

```sh
apple2 -root -mode basic -duration 236 -tv-color 400 -tv-tint 9 -tv-brightness -34.1667 -tv-contrast 263
```

#### Custom:

*The third command uses [reADDer](https://github.com/yesmaybenookay/reADDer)*

```sh
apple2 -text -program 'od -txCz -w7 /dev/urandom'
apple2 -text -program 'cat /dev/random'
apple2 -root -mode text -tv-color 400 -tv-tint 9 -tv-brightness -34.1667 -tv-contrast 263 -program 'cd /PATH/TO/reADDer/ && python reADDer.py'
```

### maze3d Settings:

#### Default Options:

```sh
maze3d [-display host:display.screen] [-visual visual] [-window]
[-root] [-speed float] [-delay number] [-fps] [-rows number] [-columns
number] [-overlay] [-wall-texture texture] [-floor-texture texture]
[-ceiling-texture texture] [-drop-acid] [-drop-acid-walls] [-drop-acid-
floor] [-drop-acid-ceiling] [-inverters number] [-rats number]
```

#### Customized Options:

```sh
maze3d -root -speed 1.21 -rows 21 -columns 21 -drop-acid -wall-texture PATH/TO/WALL_TEXTURE.jpg -floor-texture PATH/TO/FLOOR_TEXTURE.jpg -ceiling-texture PATH/TO/CEILING_TEXTURE.jpg -inverters 21 -rats 21
```

### Phosphor Settings:

*Prints output from [GodSpeaks](https://github.com/rethyxyz/godspeaks), a copy of Terry A. Davis's (R.I.P.) God Speaks program.*

```sh
phosphor -root -scale 3 -ticks 5 -delay 35000 -program "cd /PATH/TO/GodSpeaks/ && python godspeaks.py" -fg red
```

*Prints output from fortune or [fortune-mod](https://github.com/shlomif/fortune-mod).*

```sh
phosphor -root -scale 2 -ticks 5 -delay 35000 -program "fortune" -fg red
```

*Prints output from fortune in ASCII banner style from figlet.*

```sh
phosphor -root -scale 1 -ticks 1 -delay 5000 -program "fortune | figlet" -fg red
```

*Prints a text file [reADDer](https://github.com/yesmaybenookay/reADDer) chooses randomly.*

```sh
phosphor -root -scale 3 -ticks 5 -delay 35000 -program "cd /PATH/TO/reADDer/ && python reADDer.py" -fg purple
```

*Faster version for using [reADDer](https://github.com/yesmaybenookay/reADDer) with ASCII Art.*

```sh
phosphor -root -scale 3 -ticks 5 -delay 1000 -program "cd /PATH/TO/reADDer/ && python reADDer.py" -fg purple
```

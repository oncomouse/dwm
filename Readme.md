# dwm - dynamic window manager

dwm is an extremely fast, small, and dynamic window manager for X.

## Applied Patches

* [moveresize](https://dwm.suckless.org/patches/moveresize/dwm-moveresize-20201206-cce77d8.diff)
* [hide vacant tags](https://dwm.suckless.org/patches/hide_vacant_tags/dwm-hide_vacant_tags-6.2.diff)
* [color emoji](https://raw.githubusercontent.com/oncomouse/patches/master/dwm-color_emoji-20210821-138b405.diff)
* [xrdb colorbar](https://raw.githubusercontent.com/oncomouse/patches/master/dwm-xrdb_colorbar-20210117-61bb8b2.diff)
* [pertag](https://raw.githubusercontent.com/oncomouse/patches/master/dwm-pertag_nobarpos-20220319-bece862.diff)
* [statuscmd](https://dwm.suckless.org/patches/statuscmd/dwm-statuscmd-20210405-67d76bd.diff)
* [noborder](https://dwm.suckless.org/patches/noborder/dwm-noborderfloatingfix-6.2.diff)
* [focusurgent](https://dwm.suckless.org/patches/focusurgent/dwm-focusurgent-20160831-56a31dc.diff)
* [rtile](https://raw.githubusercontent.com/oncomouse/patches/master/dwm-rtile-20210619-61bb8b2.diff)
* [xsession](https://raw.githubusercontent.com/oncomouse/patches/master/dwm-xsession-20210706-61bb8b2.diff)
* [focusedontop](https://raw.githubusercontent.com/oncomouse/patches/master/dwm-focusedontop-20210917-a786211.diff)
* [autostart](https://dwm.suckless.org/patches/autostart/dwm-autostart-20210120-cb3f58a.diff)
* [systray](https://dwm.suckless.org/patches/systray/dwm-systray-6.3.diff)
* [compton floating](https://raw.githubusercontent.com/oncomouse/patches/master/dwm-compton_floating-20220320-bece862.diff)
* [picom border fixing](https://raw.githubusercontent.com/oncomouse/patches/master/dwm-picom_border_fix-20220329-bece862.diff)
* [raiseonfocus](https://raw.githubusercontent.com/oncomouse/patches/master/dwm-raiseonfocus-20220409-bece862.diff)
* [maximize](https://raw.githubusercontent.com/oncomouse/patches/master/dwm-maximize-20220320-bece862.diff)

## Requirements

In order to build dwm you need the Xlib header files.

## Installation

Edit config.mk to match your local setup (dwm is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install dwm (if
necessary as root):

```
make clean install
```

## Running dwm

Add the following line to your .xinitrc to start dwm using startx:

```
exec dwm
```

In order to connect dwm to a specific display, make sure that
the DISPLAY environment variable is set correctly, e.g.:

```
DISPLAY=foo.bar:1 exec dwm
```

(This will start dwm on display :1 of the host foo.bar.)

In order to display status info in the bar, you can do something
like this in your .xinitrc:

```
while xsetroot -name "`date` `uptime | sed 's/.*,//'`"
do
	sleep 1
done &
exec dwm
```

## Configuration

The configuration of dwm is done by creating a custom config.h
and (re)compiling the source code.

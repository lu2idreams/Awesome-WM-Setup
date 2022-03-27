# AwesomeWM Setup

Mostly for personal use. Fairly basic setup including a gruvbox theme, as well as volume, battery and network widget.

## Installation

First, install awesome, along with some of the default programs this build depends on: awesome, rofi, network-manager, nitrogen (for setting a wallpaper), urxvt/rxvt-unicode, vim, and lightdm (or some other display manager; not necessary, but recommended). The defaults may be changed later in .config/awesome/rc.lua. Afterwards, clone this repository using

```git clone https://github.com/lu2idreams/Awesome-WM-Setup/```

In case awesomewm did not create its own directory inside .config/, do so manually:

```mkdir .config/awesome/```

Change into the folder you cloned in the first step, move the rc.lua into the "awesome" directory you just created and the "theme.lua" to /usr/share/awesome/themes/default/ (you may need to delete the old theme.lua first):

```
cd Awesome-WM-Setup/
mv rc.lua ~/.config/awesome/
mv theme.lua /usr/share/awesome/themes/default/

```
To get the gruvbox theme for the default terminal emulator (urxvt) as well, you should mode the .Xresources file into your home directory (you may need to remove any existing one first)

```mv .Xresources ~/.Xresources```

If you want to use the .bashrc as well, it also needs to be placed inside your home directory.

```mv .bashrc ~/.bashrc```

Next, if you want to use the volume and battery widget, you will need to install streetturtle's (https://github.com/streetturtle/) awesomewm widgets. To do so, you need to clone the repo inside your .config/awesome/ directory:

```
cd ~/.config/awesome/
git clone https://github.com/streetturtle/awesome-wm-widgets

```

Lastly, I recommend aprilove's (https://github.com/aprilove/) collection of gruvbox wallpapers for some nice wallpapers to go along with the setup. Clone them for example into your pictures folder:

```
cd ~/Pictures/
git clone https://github.com/aprilove/Gruvbox-Wallpapers

```

To set a wallpaper consistently, use nitrogen. The Setup uses largely default keybindings, with Mod4 (Windows/Super-key) as the Modkey.

**Mod-R:** launch run-prompt (by default rofi)

**Mod-Enter:** launch terminal (by default urxvt)

**Mod-Space:** Toggle client between floating and tiling (**Mod-RMB** near a window corner to resize floating clients)

**Mod-J/K:** Select window

**Mod-H/L:** Resize master

*Known issues:* Firefox sometimes refuses to tile appropriately, in most cases hitting **Mod-Space** in case it is set to floating, or **Mod-M** in case it is set to monocle get firefox to behave properly.

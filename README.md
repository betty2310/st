# St (Suckless Terminal)

## Demo

<img src="https://raw.githubusercontent.com/betty2310/file/main/st/st.png"> <br><br>
Japanese, Vietnamese, icons and image render perfect. 
## Dependencies

```
# Debian (and ubuntu probably)
apt install build-essential libxft-dev libharfbuzz-dev

(most of these are already installed on Arch based distros)

# Install font-symbola and libXft-bgra
```

## Install

```
git clone https://github.com/betty2310/st.git
cd st
sudo make install
xrdb merge pathToXresourcesFile
```

(note : put the xrdb merge command in your wm's autostart or similar)

## Fonts

- Install JetbrainsMono Mono Nerd Font or any nerd font from [here](https://www.nerdfonts.com/font-downloads)

## Patches:

- alpha
- Ligatures
- sixel (check sixel branch)
- scrollback
- Clipboard
- Alpha(Transparency)
- Boxdraw
- patch_column ( doesnt cut text while resizing)
- font2
- right click paste
- st desktop entry
- newterm
- anygeometry
- xresources
- sync patch ( Better draw timing to reduce flicker/tearing and improve animation smoothness )
- live reload ( change colors/fonts on the fly )
  and more...
  <br>

## Default Keybindings<br>

| Keybind                     | Action                |
| --------------------------- | --------------------- |
| <kbd>super + ,</kbd>        | Zoom in               |
| <kbd>super + .</kbd>        | Zoom out              |
| <kbd>super + g</kbd>        | Reset zoom            |
| <kbd>ctrl + shift + c</kbd> | Copy                  |
| <kbd>ctrl + shift + v</kbd> | Paste                 |
| <kbd>super + s</kbd>        | Increase Transparency |
| <kbd>super + a</kbd>        | Decrease Transparency |
| <kbd>super + m</kbd>        | Reset Transparency    |
| <kbd>super + k</kbd>        | Scroll up             |
| <kbd>super + j</kbd>        | Scroll down           |

## Themes/Fonts used

- ls-icons: https://github.com/Yash-Handa/logo-ls <br>
- Theme: [nord](https://www.nordtheme.com/)
- Font: JetbrainsMono Nerd Font + material design icon fonts

# Credits

- [live-reload](https://github.com/nimaipatel/st)
- [patch_column](https://github.com/nimaipatel/st/blob/all/patches/7672445bab01cb4e861651dc540566ac22e25812.diff)

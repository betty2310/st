# St (Suckless Terminal)

## Demo

<img src="https://s3.us-west-2.amazonaws.com/secure.notion-static.com/cd369192-aaac-4df1-9bde-7406caac1f17/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220120%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220120T063300Z&X-Amz-Expires=86400&X-Amz-Signature=a191bb25647b48caacf6dfb9a0f7a602fd5dddf91eced2fa0aa8fc0ad54e0146&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject"> <br><br>

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
#### Keyboard
| Keybind | Action |
| --- | --- |
| <kbd>super + ,</kbd> | Zoom in |
| <kbd>super + .</kbd> | Zoom out |
| <kbd>super + g</kbd> | Reset zoom |
| <kbd>ctrl + shift + c</kbd> | Copy |
| <kbd>ctrl + shift + v</kbd> | Paste |
| <kbd>super + [1-0]</kbd> | View tag AKA change workspace (for you i3 folks) |
| <kbd>super + shift + [1-0]</kbd> | Move focused client to tag |
| <kbd>super + s</kbd> | Tiling layout |
| <kbd>super + shift + s</kbd> | Floating layout |
| <kbd>super + w</kbd> | Maximized / Monocle layout |
| <kbd>super + [arrow keys]</kbd> | Change focus by direction |
| <kbd>super + [hjkl]</kbd> | ^ |
| <kbd>super + shift + [arrow keys]</kbd> | Move client by direction. Move to edge if it is floating. |
| <kbd>super + shift + [hjkl]</kbd> | ^ |
| <kbd>super + control + [arrow keys]</kbd> | Resize client |
| <kbd>super + control + [hjkl]</kbd> | ^ |
| <kbd>super + f</kbd> | Toggle fullscreen |
| <kbd>super + m</kbd> | Toggle maximize |
| <kbd>super + n</kbd> | Minimize |
| <kbd>super + shift + n</kbd> | Restore minimized |
| <kbd>super + c</kbd> | Center floating client |
| <kbd>super + u</kbd> | Jump to urgent client (or back to last tag if there is no such client) |
| <kbd>super + b</kbd> | Toggle bar |
| <kbd>super + =</kbd> | Toggle tray |
<pre>
ctrl + shift + c        Copy  <br>
ctrl + shift + v        Paste <br>
right click on the terminal ( will paste the copied thing ) 

(Zoom)
alt  + comma            Zoom in <br>
alt  + .                Zoom out <br>
alt  + g                Reset Zoom<br>

(Transparency)
alt  + s                Increase Transparency<br>
alt  + a                Decrease Transparency<br>
alt  + m                Reset Transparency<br>

alt + k                 scroll down 
alt + j                 scroll up

mod + shift + enter    open a new terminal with same cwd ( current working directory )
</pre>

you can change all of these in config.h
<br>

## Themes/Fonts used

- ls-icons: https://github.com/Yash-Handa/logo-ls <br>
- Theme: [nord](https://www.nordtheme.com/) 
- Font: JetbrainsMono Nerd Font + material design icon fonts

# Credits

- [live-reload](https://github.com/nimaipatel/st) 
- [patch_column](https://github.com/nimaipatel/st/blob/all/patches/7672445bab01cb4e861651dc540566ac22e25812.diff)



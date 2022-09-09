## Arcolinux Config

<img src="https://i.imgur.com/ZhSXFde.png" alt="arcolinux"/>

### Initial Setup
```sh
# pacman -Su;
pacman -S archlinux-keyring; pacman -Syu;
```
```sh
rm -r ~/.config/qtile/ ~/.config/alacritty/;
git clone ;
cp -r ~/Downloads/arcolinux-dotfiles/* ~/.config/
```

### Fonts and Icons
```sh
pacman -S noto-fonts-emoji
yay -S nerd-fonts-complete-starship
```

### Alacritty
```sh
rm -r ~/.config/alacritty/;
cp -r ~/Downloads/arcolinux-dotfiles/alacritty ~/.config/
```

### Qtile

```sh
sudo pacman -S qtile alsa-utils canto-daemon cmus jupyter_console khal libpulse lm_sensors moc python-dbus-next python-iwlib python-keyring python-mpd2 python-psutil python-pywlroots python-setproctitle python-pyxdg xorg-xwayland python-pip pcmanfm;
pip install psutil
```

### Rofi
```sh
sudo pacman -S rofi papirus-icon-theme;
git clone https://github.com/davatorium/rofi-themes.git;
sudo cp rofi-themes/User\ Themes/onedark.rasi /usr/share/rofi/themes;
```
```sh
# delete this line in: /usr/share/rofi/themes/onedark.rasi
font: "Knack Nerd Font 14";
```
```sh
# add this line
purple: #C678DD;
```

### Picom
```sh
cp -r ~/Downloads/arcolinux-dotfiles/picom ~/.config/
```

### Starship Prompt
```sh
sudo pacman -S starship
cp ~/Downloads/arcolinux-dotfiles/starship.toml ~/.config/
```

### Fish Shell
```sh
sudo pacman -S fish exa;
cp -r ~/Downloads/arcolinux-dotfiles/fish/ ~/.config/

# change shell
echo /usr/local/bin/fish | sudo tee -a /etc/shells
chsh -s /usr/bin/fish;
```

### XMonad
```sh
# delete existing xmonad config
sudo rm -r ~/.xmonad/ ~/.xmobarrc;
# add my config
cp -r ~/Downloads/arcolinux-dotfiles/xmonad ~/.config/
cp -r ~/Downloads/arcolinux-dotfiles/xmobar ~/.config/
```

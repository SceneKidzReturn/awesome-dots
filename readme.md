# Setup
**1. Install:**
```bash
yay -S picom-git awesome-git acpid git mpd ncmpcpp wmctrl \
firefox lxappearance gucharmap thunar alacritty neovim polkit-gnome \
xdotool xclip scrot brightnessctl alsa-utils pulseaudio jq acpi rofi \
inotify-tools zsh mpdris2 bluez bluez-utils bluez-plugins acpi acpi_call \
playerctl redshift cutefish-cursor-themes-git cutefish-icons upower xorg xorg-init task````
----------------------------------------------------------------------------------------------
**2. Clone Repo:**
```bash
cd
clear
git clone --recurse-submodules https://github.com/saimoomedits/dotfiles.git
cd dotfiles````
----------------------------------------------------------------------------------------------
**3. Copy the dotfiles in required places:**
```bash
mkdir ./themes
cp -rf .config/* ~/.config/
cp -rf extras/mpd ~/.mpd
cp -rf extras/ncmpcpp ~/.ncmpcpp
cp -rf extras/fonts ~/.fonts
cp -rf extras/scripts ~/.scripts
cp -rf extras/oh-my-zsh ~/.oh-my-zsh
cp -rf extras/themes/* ./themes
````
----------------------------------------------------------------------------------------------
**4. Extract GTK Themes:**
```bash
mkdir ~/.themes
cp ./themes/* ~/.themes
cd ~/.themes
tar -xf Awesthetic.tar
tar -xf Cutefish-light-modified.tar
rm Awesthetic.tar Cutefish-light-modified.tar
````
----------------------------------------------------------------------------------------------
**5. Extra:**
```bash
cd ~/.config/awesome/misc
sudo chmod -R +x *
````
----------------------------------------------------------------------------------------------
**6: Startup Services:**
```bash
systemctl --user enable mpd
sudo systemctl enable bluetooth
````
----------------------------------------------------------------------------------------------
**7. Other Important Steps:**
```bash
cd
cd dotfiles/
git clone https://github.com/SceneKidzReturn/awesome-dots
cd awesome-dots/
mv awesome/ ~/.config/awesome/
cd
pkill awesome
````

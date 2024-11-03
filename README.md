# My Hypr Dotfiles
### This is based on Hyprdots/HyDE project. Show them some love
Installing HyDE after minimal archinstall installs conflicting network managers which can cause disconnects. 
Run this to fix that

```
sudo systemctl disable --now iwd.service
sudo pacman -R iwd
sudo systemctl restart NetworkManager.service
```
You need to reboot after that

### Setting up Hyprlock
switched to Hyprlock because funny animation and weather and image and <br>
To switch to swaylock again, check layout_1 and layout_2 in ~/config/wlogout/ <br>
Also change keybinding in ~/.config/hypr/keybindings.conf <br>

### Switching to Hyprpanel
[Hyprpanel](https://hyprpanel.com/getting_started/installation.html) is cool and pogger and sexy and pog and <br>
The keybindings for waybar are commented out incase i plan to move back. The gamemode.sh in the .local/share/bin folder has been updated to not start waybar haha. Hyprpanel conf has been added. just importing it should workey?

### Using Waypaper with HyDE
1. yay -S waypaper
2. edit /home/,config/waypaper/config.ini to add `post_command = /home/quiet/.local/share/bin/swwwallpaper.sh -s $wallpaper`
3. Now waypaper should change wallpaper using the scripts in HyDE so that cache is built and works well with hyprlock and stuff.
<br>
Made this because i was kinda tired of having to call my wallpapers to the themes folder lmao <br>
### Directories i keep forgetting
1. sddm themes `/usr/share/sddm/themes`, sddm config `/etc/sddm.conf.d/`
2. scripts path ` .local/share/bin`
3. grub themes `/etc/default/grub`

### Required packages to show album art in swaync
1. `yay -S gvfs` <br>
[Updating grub](https://github.com/OliveThePuffin/yorha-grub-theme)


### chezmoi guide
1. ![chezmoi quick start](https://www.chezmoi.io/quick-start/#start-using-chezmoi-on-your-current-machine)
2. To use chezmoi to do the dotfile thingy, run `chezmoi init git@github.com:notquitethereyet/hyprdots.git`
3. Then run this `chezmoi update -v` 
![state mandated fetch screenshot](https://github.com/notquitethereyet/dotfiles/blob/main/hyprdots.png?raw=true)
![wife lockscreen](https://github.com/notquitethereyet/dotfiles/blob/main/hyprlock.png?raw=true)


# HyprV3

> Warning: this script might not work as expected due to the convert to paru. I'm working on this convert but its not there yet for a stable use.

This is V3 of the Hyprland install script

collection of dot config files for hyprland with a simple install script for a fresh Arch linux with paru

You can grab the config files and install packages by hand with this command

Do this ONLY if you need Nvidia support (do this first)

```
paru -S linux-headers nvidia-dkms qt5-wayland qt5ct libva libva-nvidia-driver-git

Add modules: nvidia nvidia_modeset nvidia_uvm nvidia_drm to /etc/mkinitcpio.conf

Generate new image: sudo mkinitcpio --config /etc/mkinitcpio.conf --generate /boot/initramfs-custom.img

Add/create the following: options nvidia-drm modeset=1 in /etc/modprobe.d/nvidia.conf

reboot!
```

Now install the below for Hyprland

```
paru -S hyprland kitty jq mako waybar-hyprland swww swaylock-effects \
wofi wlogout xdg-desktop-portal-hyprland swappy grim slurp thunar \
polkit-gnome python-requests pamixer pavucontrol brightnessctl bluez \
bluez-utils blueman network-manager-applet gvfs thunar-archive-plugin \
file-roller btop pacman-contrib starship ttf-jetbrains-mono-nerd \
noto-fonts-emoji lxappearance xfce4-settings sddm-git sddm-sugar-candy-git
```

Or you can use the attached script "set-hypr" to install everything for you.

# LinuxFarsiFont
XML Config for making Farsi/Arabic fonts of a Linux system looks better

# Prerequisties:
Make sure you have Sahel font installed on your system or change `Sahel` in `10-sahel.conf` file to something you like or you have installed on your system.

# How to use:
Copy `10-sahel.conf` file to this path. (Create subdirectories as needed):
```
cp 10-sahel.conf $HOME/.config/fontconfig/conf.d/10-sahel.conf
```
After copying the config file, you need to rebuild your *fontconfig* cahce:
```
fc-cache
```
Log out and log back in for changes to take effect.

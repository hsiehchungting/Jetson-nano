# install VINO – VNC Server
<p align="center">
  <img src="https://github.com/hsiehchungting/Jetson-nano/blob/master/Remote-VINO/vino screen.jpg" width="280">
</p>

# VINO-VNC Server
This is a way help you can remote control your nano by vino.


# install vino

```
sudo apt update
sudo apt install vino
```

#let you don't need check your password again!
```
gsettings set org.gnome.Vino prompt-enabled false
gsettings set org.gnome.Vino require-encryption false
```

#show your network card number
```
nmcli connection show 
```
```
dconf write /org/gnome/settings-daemon/plugins/sharing/vino-server/enabled-connections "['填入這裏/your network card number']"
```
```
export DISPLAY=:0
```
#start your vnc server
```
/usr/lib/vino/vino-server
```

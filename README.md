# kali-linux-virtual-machine

### Keyboard
How to set persistent keyboard layout for Kali Linux?

edit `/etc/default/keyboard`

### WiFi devices
How to enable support for WiFi devices based on Atheros AR9271 and AR7010 chipsets?

edit `/etc/apt/sources.list` and add the line

`deb http://httpredir.debian.org/debian/ jessie main contrib non-free`


Then, run the command
```bash
sudo apt-get update && sudo apt-get install firmware-atheros
```

### Start SSH automatically on boot
```bash
sudo systemctl enable ssh
```


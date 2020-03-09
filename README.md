# kali-linux-virtual-machine

### Torrent for VMware-Fusion-Pro-11.5.1

[Lint to Torrent for VMware-Fusion-Pro-11.5.1](https://github.com/apierr/kali-linux-virtual-machine/raw/master/VMware-Fusion-Pro-11.5.1.extended_Torrentmac.net.zip.torrent)

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

### Running shell as super user
```bash
sudo -s
```

### Connecting to a WiFi network using Linux command line
Reference: [https://linuxcommando.blogspot.com/2013/10/how-to-connect-to-wpawpa2-wifi-network.html](https://linuxcommando.blogspot.com/2013/10/how-to-connect-to-wpawpa2-wifi-network.html)

```bash
sudo -s
ip link set wlan0 up
/sbin/iw wlan0 link # Check the connection status
sudo /sbin/iw wlan0 scan
wpa_passphrase <SSID> >> /etc/wpa_supplicant.conf 
# ...type in the passphrase and hit enter...
cat /etc/wpa_supplicant.conf 
sudo wpa_supplicant -B -D wext -i wlan0 -c /etc/wpa_supplicant.conf
/sbin/iw wlan0 link
```


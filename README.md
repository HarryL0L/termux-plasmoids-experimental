# termux-plasmoids-experimental

```
cat /data/data/com.termux/files/usr/bin/android-wifi
#!/data/data/com.termux/files/usr/bin/bash
termux-wifi-connectioninfo | jq -r '"\(.ssid)|\(.rssi)|\(.ip)|\(.link_speed)"'

cat /data/data/com.termux/files/usr/bin/android-battery
#!/data/data/com.termux/files/usr/bin/bash
termux-battery-status | jq -r '"\(.percentage)|\(.status)"'
```

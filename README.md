termux-plasmoids-experimental

---

📦 Requirements

pkg install jq termux-api

Also make sure you have the Termux:API app installed.

---

⚙️ Setup

1. Wi-Fi Script

Create the file:

`nano $PREFIX/bin/android-wifi`

Paste:

```bash
#!/data/data/com.termux/files/usr/bin/bash
termux-wifi-connectioninfo | jq -r '"\(.ssid)|\(.rssi)|\(.ip)|\(.link_speed)"'
```


Make it executable:

`chmod +x $PREFIX/bin/android-wifi`

---

2. Battery Script

Create the file:

`nano $PREFIX/bin/android-battery`

Paste:

```bash
#!/data/data/com.termux/files/usr/bin/bash
termux-battery-status | jq -r '"\(.percentage)|\(.status)"'
```

Make it executable:

`chmod +x $PREFIX/bin/android-battery`

---

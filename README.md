# Raspi5Image

To begin setup, on any Raspberry Pi OS (for the pi5) ensure you are the root user: `sudo su root`

Once in root execute:
```
git clone https://github.com/OneH2/Raspi5Image.git
cd Raspi5Image/
chmod 777 raspi5Setup.sh
./raspi5Setup.sh
```

Note: if you are having internet issues, check to see if:
  1. The settings applied during Raspberry Pi Imager's SD card burn are correct for whatever wifi SSID and pass you have
  2. wlan0 is present amoung the interfaces listed using `ifconfig`
  3. wlan0 has a higher metric than usb0 or eth0 using `ip route`
     A. if not, execute: `sudo nmcli con mod 'preconfigured' ipv4.route-metric 0` and reboot

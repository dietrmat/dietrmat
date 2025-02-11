# Flashing ESP32 WROOM

```bash
# Add user to uucp group to allow access to serial ports
sudo gpasswd --add ${USER} uucp

# Install esptool since web.esphome.io is not working properly
pipx install esptool

# Connect ESP32 and find proper serial port
ls -l /dev/ttyUSB*

# Check if everything works by checking the ID of the ESP32
esptool.py --port /dev/ttyUSB0 flash_id

# For some esp32 chips esptool seems to has problems talking to the device.
# In this case the --no-stub option can help
esptool.py --no-stub --port /dev/ttyUSB0 flash_id

# After determing flash_id with --no-stub the device can be accessed normally again
esptool.py --port /dev/ttyUSB0 erase_flash

# Write your own image (4 minute)
esptool.py --port /dev/ttyUSB0 write_flash 0x0 /path/to/<image>.bin
```

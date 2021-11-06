# Downloading and Flashing MicroPython Firmware with esptool.py

Unlike other boards, MicroPython isn’t flashed onto the ESP32 or ESP8266 by default.  
That’s the first thing you need to do to start programming your boards with MicroPython: flash/upload the firmware.

## Installing esptool.py
To work with esptool.py, you’ll need either Python 3.7.

```pip3 install esptool```

After installing, you will have esptool.py installed into the default Python executables directory and you should be able to run it with the command esptool.py.  
In your Terminal, run the following command:

```esptool.py```


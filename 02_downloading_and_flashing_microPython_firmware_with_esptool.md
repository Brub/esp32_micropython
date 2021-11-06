# Downloading and Flashing MicroPython Firmware with esptool.py

Unlike other boards, MicroPython isn’t flashed onto the ESP32 or ESP8266 by default.  
That’s the first thing you need to do to start programming your boards with MicroPython: flash/upload the firmware.

## Installing esptool.py
To work with esptool.py, you’ll need either Python 3.7.

```pip3 install esptool```

After installing, you will have esptool.py installed into the default Python executables directory and you should be able to run it with the command esptool.py.  
In your Terminal, run the following command:

```esptool.py```

With esptool.py installed in your computer, you can easily flash your ESP32 or ESP8266 boards with the MicroPython firmware.

## Downloading MicroPython Firmware for ESP32
To download the latest version of MicroPython firmware for the ESP32, go to the [MicroPython Downloads page](https://micropython.org/download/#esp32) and scroll all the way down to the ESP32 section.

## Define which port to use
The easist way to check which port to use for connecting to the ESP32 on a mac is to run the following command in the terminal without connected and connected esp32
```ls /dev/tty*```  
Now you will something like this ```/dev/tty.usbserial-1410```

## Erase the flash
If you are putting MicroPython on your board for the first time then you should first erase the entire flash using the following command in the terminal  
```esptool.py --chip esp32 --port /dev/tty.usbserial-1410 erase_flash```

## Flashing MicroPython Firmware on ESP32
Open a terminal where the firmwhare is downloaded and use the following command to flash MicroPython Firmware on ESP32  
```esptool.py --chip esp32 --port /dev/tty.usbserial-1410 --baud 115200 write_flash -z 0x1000 esp32-20210902-v1.17.bin````  

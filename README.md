# TILTPILLHUB
TILTPILLHUB CLOUD => https://tiltpillhub.bubble-logger.com/login.php

### What is TILTPILLHUB
TILTPILLHUB is a fermentation logger capturing the TILT hydrometer or RAPT PILL data of gravity and temperature by Bluetooth.

It is based on ESP32 and supports Shelly Plugs and Sonoff BASIC R3 for controlling a fridge or heater and hence secondly acts as a temperature controller. These plugs is controlled over local network by HTTP commands.

All data and controlling is done at TILTPILLHUB CLOUD and hence you only need to enter wifi details once in the logger.
![Overview_TILTPILLHUB](https://user-images.githubusercontent.com/16992918/216659475-5f0e1974-2800-446a-8781-19560506e31d.png)

### Parts needed
An ESP32, a usb cord and a TickTax box to hold it all, and ensure some moisture protection. A magnet can help hold it in place, so you might consider to glue one on for metal fermenters. Currently, it have been tested with ESP32 DevKit1, ESP32S NodeMCU, and Wemos ESP32 D1 Mini. If you wish to use the TempControl function you will need Shelly Plugs and/or Sonoff BASIC R3 the later setup in DIY mode.

### Installing and Download
As TILTPILLHUB run on same database as iBLOPPER you can see how to setup and install at => https://iblopper.bubble-logger.com/iblopper-esp32-building/. The Binfile and files to setup you will find under releases.

> 1. Install CP210x USB to UART Bridge VCP Drivers, if not already done.
> 2. Ensure ESP32 is pugged into USB.
> 3. Go to “Devices” (e.g. use win10/11 search and write “devices”).
> 4. Under “Ports” in Devices. Notice this USB port number for “CP210x USB to UART”!
> 5. Open and edit “Erase_USB_COMX” and set correct port (eg. change the port number ONLY): esptool.exe -p COM4 -b 115200 erase_flash
> 6. Run “Erase_USB_COMX” to ensure ESP32 is clean.
> 7. Open and edit the “SETUP_USB_COMX” to reflect the port you using, eg. change the port number ONLY: esptool.exe --chip esp32 --port COM4 --baud 921600 --before default_reset --after hard_reset write_flash -z --flash_mode dio --flash_freq 80m --flash_size detect 0xe000 boot_app0.bin 0x1000 bootloader_dio_80m.bin 0x10000 TILTPILLHUB1.0.0.bin 0x8000 iBLOPPER4.ino.partitions.bin
> 8. Hit and run the “Window batch file” named “SETUP_USB_COMX”
Now the iBLOPPPER`ESP32 software get installed.


NOTICE!

Please remember to hold and press “BOOT” when you see “…………..——–…………………….———” during upload/install of the ESP32.
If updating to new build and/or making use of an ESP32 from earlier project, ensure to erase everything as else you will get instability issues.
Secondly, always pull the power from iBLOPPER´ESP32 after installing before setting it up.
If something goes wrong you can erase everything after editing accordingly as above by running “Erase_USB_COMX” (esptool.exe -p COM4 -b 115200 erase_flash). 



### Setup at TILTPILLHUB CLOUD => https://tiltpillhub.bubble-logger.com/login.php
Power on the logger. Setup the wifi by joining the Portal of the logger by ip 192.168.4.1 (if it do not come up by it self). You will need the 8-10 ciffer (chip id of ESP32) number as seen when setting up wifi for logger so notice it, and use this number as you Username when creating an account at TILTPILLHUB CLOUD. That is it. TILTPILLHUB CLOUD => https://tiltpillhub.bubble-logger.com/login.php


### A bit more overview of what TILTPILLHUB can do in picture form
![image](https://user-images.githubusercontent.com/16992918/216809032-98bf817e-a162-4207-a665-04aed202ca81.png)

## Some further screenshorts
### Main screen
![image](https://user-images.githubusercontent.com/16992918/216788917-1569b3a0-4c08-4a9e-9c27-91df3fff3a58.png)


### Veiw/share brew Screen
![image](https://user-images.githubusercontent.com/16992918/216789024-15e3a990-3583-4d75-8583-ae5cf55afecb.png)

### Log A Brew Screen
![image](https://user-images.githubusercontent.com/16992918/216789318-87deee3c-e273-47f5-9465-6eb0c4b91547.png)


### Settings Screen
![image](https://user-images.githubusercontent.com/16992918/216789124-f452e544-cf83-43fc-aa21-390bf836e638.png)

### TempControl Settings Screen
![image](https://user-images.githubusercontent.com/16992918/216789162-248eedf7-e19f-445e-830f-cda7d4551c6e.png)



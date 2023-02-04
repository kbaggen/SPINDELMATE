# TILTPILLHUB
TILTPILLHUB CLOUD => https://tiltpillhub.bubble-logger.com/login.php

TILTPILLHUB is a fermentation logger capturing the TILT hydrometer or RAPT PILL data of gravity and temperature by Bluetooth.

It is based on ESP32 and supports Shelly Plugs and Sonoff BASIC R3 for controlling a fridge or heater and hence secondly acts as a temperature controller. These plugs is controlled over local network by HTTP commands.

All data and controlling is done at TILTPILLHUB CLOUD and hence you only need to enter wifi details once in the logger.
![Overview_TILTPILLHUB](https://user-images.githubusercontent.com/16992918/216659475-5f0e1974-2800-446a-8781-19560506e31d.png)


As TILTPILLHUB run on same database as iBLOPPER you can see how to setup and install at => https://iblopper.bubble-logger.com/iblopper-esp32-building/.


> 1). Install CP210x USB to UART Bridge VCP Drivers, if not already done.
> 2). done this before.
> 3.) Ensure ESP32 is pugged into USB.
4.) Go to “Devices” (e.g. use win10/11 search and write “devices”).
5). Under “Ports” in Devices. Notice this USB port number for “CP210x USB to UART”!
6). Open and edit “Erase_USB_COMX” and set correct port (eg. change the port number ONLY): esptool.exe -p COM4 -b 115200 erase_flash
7). Run “Erase_USB_COMX” to ensure ESP32 is clean.
8). Open and edit the “SETUP_USB_COMX” to reflect the port you using, eg. change the port number ONLY: esptool.exe --chip esp32 --port COM4 --baud 921600 --before default_reset --after hard_reset write_flash -z --flash_mode dio --flash_freq 80m --flash_size detect 0xe000 boot_app0.bin 0x1000 bootloader_dio_80m.bin 0x10000 TILTPILLHUB1.0.0.bin 0x8000 iBLOPPER4.ino.partitions.bin
9). Hit and run the “Window batch file” named “SETUP_USB_COMX”
Now the iBLOPPPER`ESP32 software get installed.

If something goes wrong you can erase everything after editing accordingly as above by running “Erase_USB_COMX” (esptool.exe -p COM4 -b 115200 erase_flash). 

NOTICE!

Please remember to hold and press “BOOT” when you see “…………..——–…………………….———” during upload/install of the ESP32.

If updating to new build and/or making use of an ESP32 from earlier project, ensure to erase everything as else you will get instability issues.

Secondly, always pull the power from iBLOPPER´ESP32 after installing before setting it up.




but basically you just need the 8-10 ciffer (chip id of ESP32) number as seen when setting up wifi for logger, and use this number as you Username when creating an account at TILTPILLHUB CLOUD. 

Binfil and istall for TILTPILLHUB is under releases here at Github.


Some screen shorts:

Main screeen!





![Overview2_TILTPILLHUB](https://user-images.githubusercontent.com/16992918/216659482-7c5874e1-c3ca-4bc6-96b4-3485cd1c1937.png)

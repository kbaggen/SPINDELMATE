# TILTPILLMATE
TILTPILLMATE CLOUD => https://tiltpillmate.bubble-logger.com/login.php

### What is TILTPILLMATE
TILTPILLMATE is a fermentation logger capturing the TILT hydrometer or RAPT PILL data of gravity and temperature by Bluetooth. Furthermore, it is a cloud service allowing to easily uploading your data.

It is based on ESP32 and supports Shelly Plugs and Sonoff BASIC R3 for controlling a fridge or heater and hence secondly acts as a temperature controller. These plugs is controlled over local network by HTTP commands.

All data and controlling is done at TILTPILLHUB CLOUD and hence you only need to enter wifi details once in the logger.
![image](https://user-images.githubusercontent.com/16992918/216826960-47a5f6e0-37d9-4002-8dcd-6df2f6ae6f54.png)


### Parts needed
An ESP32, a usb cord and a TickTax box to hold it all, and ensure some moisture protection. A magnet can help hold it in place, so you might consider to glue one on for metal fermenters. Currently, it have been tested with ESP32 DevKit1, ESP32S NodeMCU, and Wemos ESP32 D1 Mini. If you wish to use the TempControl function you will need Shelly Plugs and/or Sonoff BASIC R3 the later setup in DIY mode.

### Installing and Download
As TILTPILLHUB run on same database as iBLOPPER you can see how to setup and install at => https://iblopper.bubble-logger.com/iblopper-esp32-building/. The Binfile and files to setup you will find under releases at GITHUB.

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



### Setup
Power on the logger. Setup the wifi by joining the Portal of the logger by ip 192.168.4.1 (if it do not come up by it self). You will need the 8-10 ciffer (chip id of ESP32) number as seen when setting up wifi for logger so notice it, and use this number as you Username when creating an account at TILTPILLCLOUD. That is it. TILTPILLCLOUD => https://tiltpillmate.bubble-logger.com/login.php


### A bit more overview of what TILTPILLMATE can do in picture form
![Overview2_TILTPILLHUB](https://user-images.githubusercontent.com/16992918/216809167-89c934cf-1837-4fd4-93a8-f659680b4091.png)

# Some further screenshorts 

### Main screen of GUI
![image](https://user-images.githubusercontent.com/16992918/216828058-57cb327c-d982-487b-91ea-8921dd5ec94f.png)



### Veiw/share brew Screen
![image](https://user-images.githubusercontent.com/16992918/216828103-2cee8475-b06a-4e3f-a93e-9c2936666bc2.png)




### Log A Brew Screen
![image](https://user-images.githubusercontent.com/16992918/216827141-b332b2c2-0c3b-4f27-9847-72126e33657a.png)


### Settings Screen
![image](https://user-images.githubusercontent.com/16992918/216810041-aa30671e-514f-4771-84d4-b316cbc8e184.png)


### TempControl Settings Screen
![image](https://user-images.githubusercontent.com/16992918/216789162-248eedf7-e19f-445e-830f-cda7d4551c6e.png)



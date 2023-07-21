<p align="center">
    <img width="400" src="https://user-images.githubusercontent.com/16992918/218797276-db2669b0-3015-4daa-a63e-b171f8bf125d.png" alt="SPINDELMATE logo">
  </p>


### What is SPINDELMATE <sup><sub>NOTICE 21 July 2023 - Seems RAPT PILL is broken as Kegland changed in dataset!!!</sup></sub>
<sup><sub>SPINDELMATE CLOUD => https://spindelmate.bubble-logger.com/login.php</sup></sub>


SPINDELMATE is a fermentation logger capturing the TILT hydrometer or RAPT PILL data of gravity and temperature by Bluetooth or WiFI signal from iSPINDEL. Furthermore, it is a cloud service allowing to easily uploading your data. NOTICE 21 July 2023 - Seems RAPT PILL is broken as Kegland changed in dataset!!!

It is based on ESP32 and supports Smart Plugs (Shelly, Sonoff in "DIY mode" and Tasmota Plugs) for controlling a fridge or heater and hence secondly acts as a temperature controller. These plugs is controlled over local network by HTTP commands.

All data and controlling is done at SPINDELMATE CLOUD and hence you only need to enter wifi details once in the logger.
![overview_x](https://user-images.githubusercontent.com/16992918/218760899-e3352de1-693a-4ffb-9fd5-a7318df9352b.png)



### Parts needed
An ESP32, a usb cord and a TickTax box to hold it all, and ensure some moisture protection. Currently, it have been tested with Wemos ESP32 d1 mini and ESP32 DevKit1 (esp-wroom-32 devkit v1), see more below. If you wish to use the TempControl function you will need Plugs from Tasmota, Shelly and/or Sonoff in DIY mode (se more below).

### Installing and Download
You can use Brewflasher (http://www.brewflasher.com/) or Webbased version (https://web.brewflasher.com/fw/108) to install SPINDELMATE. You will need to Install "CP210x USB to UART Bridge VCP Drivers" first though, please see below.

If you wish for manual install (a bit faster for updates):
> 1. Install CP210x USB to UART Bridge VCP Drivers (https://www.silabs.com/developers/usb-to-uart-bridge-vcp-drivers) so you PC can find and see the ESP32.
> 2. Install ESP Home Flasher (https://github.com/esphome/esphome-flasher/releases), e.g. flash program to flash install-bins onto the ESP32. The flash program also give your the possibility to see and view what going on inside logger.
> 2. Or you can use the Update function in the AP portal when powering on the logger if SPINDELMATE already installed in earlier version. 
> 3. Download and run the Install-bin files accordingly in ESP Home Flasher (or AP portal). You find the install .bin file under releases here at Github (https://github.com/kbaggen/SPINDELMATE/releases).
NOTICE! Please remember to hold and press “BOOT” during the start of upload to the ESP32 until after it states "Chip Info"!


### Setup (at https://spindelmate.bubble-logger.com/login.php)
Power on the logger. Setup the wifi by joining the Portal of the logger by ip 192.168.4.1 (if it do not come up by it self). You will need the 8-10 ciphers (chip id of ESP32) there appears when entering AP mode later so notice it, and use this number as you __Username__ when creating an account at SPINDELMATE CLOUD. That is it. 


### Behavior
The first 60 sec´s after power on it will light blue in AP mode and hence you can set Wifi credentials. Thereafter in will turn blue LED off, and only flash it every 10 sec´s where it ping the iBeacon signal (repeats/boots the  TILT signal or emulate a TILT Bluetooth signal for RAPT PILL or iSPINDEL users). After the "cycle in min" time you have set in settings has ended it will scan for TILT or RAPT Pill according till the "cycle in min" setting. NOTICE 21 July 2023 - Seems RAPT PILL is broken as Kegland changed in datasetMeaning if 3 mins is set it scan for 30-120 secs after those 3 minutes, and if 6 mins is set it will scan after 6 minutes for 60-240 secs, where the later then supports a telemetric setting of every 3rd min for a RAPT PILL. As the TILT pings every 10 sec, it should be covered however you do set the cycle behavior.

If using SPINDELMATE for iSPINDEL, it will as soon as it dectect the iSPINDEL turn off the above Bluetooth scanning of TILT/RAPT Pill. For iSPINDEL you must include the iSPINDEL Chip ID at settings at SPINDELMATE Cloud. To send from iSPINDEL till SPINDELMATE both must be on same local network so you will need to find the ip of SPINDELMATE (see in router, or use serial output of Brewflasher, Arduino IDE or Esphome-flasher as SPINDELMATE state the local IP during startup) and enter SPINDELMATE ip in iSPINDEL e.g. 192.168.x.x (+ use port 80 and "/" as patch) and choose HTTP as sending mode. It should send temperature in celsius. For iSPINDEL use see more here: https://iblopper.bubble-logger.com/2352-2/

### ESP32 supported
If you wish to buy one you should go for: 

ESP32 DevKit1 or ESP32 D1 mini 

Please Read More at Wiki --> https://github.com/kbaggen/SPINDELMATE/wiki/Supported-ESP32


### Other sensors supported
You can monitor your yeast activity by motioning the CO2 blops pr. minute (BPM). Two differnt sensors is supported.

You can either use a MPU6050 to follow the bubble/CO2 release by vibration techonology for both S-airlock or the 3-pieces type. Or you can use a LM393 sound sensor. The later fits perfectly into a S-airlock "head", and by adding a smal water ballon for moisture protection you can detects the sound when CO2 is released.
Read more at Wiki -- > https://github.com/kbaggen/SPINDELMATE/wiki/Activity-sensor:-MPU6050-or-LM393-Sound-sensor-for-Blops-pr.-Min-(BPM)-detection

### Plugs supported
__The following is tested and working:__

Sonoff Basic R3, Shelly PLUG S (@admin), Shelly PLUS PLUG US and TASMOTA Martin Jerry Mini Smart Plug (@Frank Nobrega), Shelly 1, Shelly 1 PM, Shelly PRO 1, Shelly PRO 1 PM (@Per F. Sørensen).

__Likkely working (from specification/API):__

Sonoff Mini, Sonof RFR3, and various Tasmota plugs.

Please Read More at Wiki --> https://github.com/kbaggen/SPINDELMATE/wiki/Temperature-Control-by-WiFI-Smart-Plug

### Limitation
You can only run one TILT or PILL by each ESP32, and also need one login (Chip ID of ESP32) accordingly for each ESP32. Sorry :-)
A strong and decent network is also a prerequisite for SPINDELMATE to work.


### A bit more overview of what TILTPILLMATE can do in picture form
![image](https://user-images.githubusercontent.com/16992918/219751073-18175fff-60c7-46ed-8214-432159c5d816.png)



# Some further screenshots 

### Main screen of GUI
![image](https://user-images.githubusercontent.com/16992918/218799876-d7dfa0f4-a9b6-445e-ab5c-a04d56ececc2.png)


### View/share brew Screen
![image](https://user-images.githubusercontent.com/16992918/218859393-85fd9d1c-1d1d-424d-92a3-e3dde90456a9.png)


### Log A Brew Screen
![image](https://user-images.githubusercontent.com/16992918/218800730-c04548ec-1387-4909-aa2b-782bdc495381.png)


### Settings Screen
![image](https://user-images.githubusercontent.com/16992918/218800202-399dfde9-65fc-4752-b04a-77f74b4a8357.png)

### TempControl Settings Screen
![image](https://user-images.githubusercontent.com/16992918/218800329-66ce1345-066b-4c41-8fc8-bb5440f4faef.png)




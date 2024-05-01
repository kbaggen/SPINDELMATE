![image](https://github.com/kbaggen/SPINDELMATE/assets/16992918/e5d08cf2-9897-4cb7-aaf8-7d3183b24085)




<sup><sub></sup></sub><sup><sub>UPDATED on 30 APRIL 2024 - versionM.5.1! SPINDELMATE USERS should now use iBLOPPER CLOUD as the 2 projects is merging, hence, for best experaince and fastest updates use iBLOPPER CLOUD and set sensitivity under settings to "0" to turn blops detection off if you wish so.</sup></sub><sup><sub>

SPINDELMATE CLOUD => iBOPPER CLOUD ~ https://bubble-logger.com/M5/login.php </sup></sub>


SPINDELMATE is a fermentation logger capturing the TILT hydrometer or RAPT PILL data of gravity and temperature by Bluetooth or WiFI signal from iSPINDEL. Furthermore, it is a cloud service allowing to easily uploading your data.

It is based on ESP32 DevKit1 and supports Smart Plug (Shelly and Tasmota Plugs) for controlling a fridge or heater and hence secondly acts as a temperature controller. These plugs is controlled over local network by HTTP commands.

All data and controlling is done at SPINDELMATE CLOUD and hence you only need to enter wifi details once in the logger.
![image](https://github.com/kbaggen/SPINDELMATE/assets/16992918/c766ef36-d9d2-42fc-97f5-2b85bfd3702b)




### Parts needed
An ESP32 DevKit1 or M5stack ATOM S3 LCD or M5stack ATOM S3 Lite, a usb cord and a TickTax box to hold it all if using ESP32, and ensure some moisture protection. If you wish to use the TempControl function you will need Plug from Tasmota or Shelly.

### Installing and Download
Please download .exe. install programs for M.5.0 version under relase (see right sidebar):
> 1. Install CP210x USB to UART Bridge VCP Drivers (https://www.silabs.com/developers/usb-to-uart-bridge-vcp-drivers) so you PC can find and see the ESP32. OR for M5stack S3 ATOM chips  Windows D2XX (https://ftdichip.com/drivers/d2xx-drivers/) drivers if needed.

> 2.Download the SPINDELMATE/iBLOPPER MATE installer at releases for either ESP32 DEVKIT1 or M5stack S3 ATom LCD or LITE

> 3. Select the USB PORT.

> 4. Install by hitting “Burn” (after M5stack ATOM S3 has showed the green light on side) .

NOTICE! Please remember to hold and press “BOOT” during the start of upload to the ESP32 until after it states "Chip Info"! For M5stack, Press button on side of M5stack ATOM S3 for 2 sec, until it light green to set it in boot-loader mode.

![image](https://github.com/kbaggen/SPINDELMATE/assets/16992918/ca3f72af-b10e-4091-aacd-0d1e9eca51bc)


### Setup (at https://spindelmate.bubble-logger.com/login.php)
Power on the logger. Setup the wifi by joining the Portal of the logger by ip 192.168.4.1 (if it do not come up by it self). You will need the 8-10 ciphers (chip id of ESP32) there appears when entering AP mode later so notice it, and use this number as you __Username__ when creating an account at SPINDELMATE CLOUD. That is it. 


### Behavior
The first 60 sec´s after power on it will light blue in AP mode and hence you can set Wifi credentials. Thereafter in will turn blue LED off, and only flash it when sending data. After the "cycle in min" time you have set in settings has ended it will scan for TILT or RAPT Pill according till the "cycle in min" setting. Meaning if 5 mins is set it scan for 50 secs after those 5 minutes, and if 6 mins is set it will scan after 6 minutes for 60 secs and so on, where the later then supports a telemetric setting of every 1 min for a RAPT PILL. As the TILT pings every 10 sec, it should be covered however you do set the cycle behavior.

If using SPINDELMATE for iSPINDEL, it will as soon as it dectect the iSPINDEL turn off the above Bluetooth scanning of TILT/RAPT Pill. For iSPINDEL you must include the iSPINDEL Chip ID at settings at SPINDELMATE Cloud. To send from iSPINDEL till SPINDELMATE you should use the AcessPoint created by SPINDELMATE "AP for ispindel xxxxx" (IP 192,168,4,1) and use port 80, "/" as patch and choose HTTP as sending mode. It should send temperature in celsius. For iSPINDEL use see more here: [iSPINDEL suuport](https://github.com/kbaggen/SPINDELMATE/wiki/iSPINDEL-support-for-SPINDELMATE)

### ESP32 supported
We support "ESP32 Devkit v1" (is sold under various names) and  M5stack ATOM S3 LCD or M5stack ATOM S3 Lite. So please go for a version with pins as picture state:
![image](https://github.com/kbaggen/SPINDELMATE/assets/16992918/6b272c9a-6601-406c-ace9-fe0f0540d553)


![image](https://github.com/kbaggen/SPINDELMATE/assets/16992918/135d8aa4-b900-4bae-9fb2-509d63786a5a)




### Plugs supported
__At time of writing the following plug has been proven to work:__

* Shelly PLUG S
* Shelly PLUS PLUG US
* TASMOTA Martin Jerry Mini Smart Plug
* Athom - Tasmota EU Plug V2
* Shelly 1
* Shelly 1 PM
* Shelly PRO 1
* Shelly PRO 1 PM

__Likkely working (from specification/API):__

various Tasmota plugs.

Please Read More at Wiki --> https://github.com/kbaggen/SPINDELMATE/wiki/Temperature-Control-by-WiFI-Smart-Plug

### Limitation
You can only run one TILT or PILL by each ESP32, and also need one login (Chip ID of ESP32) accordingly for each ESP32. Sorry :-)
A strong and decent network is also a prerequisite for SPINDELMATE to work.


### A bit more overview of what TILTPILLMATE can do in picture form
![image](https://github.com/kbaggen/SPINDELMATE/assets/16992918/d2f1c458-605b-4258-af41-631b20b027d0)



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




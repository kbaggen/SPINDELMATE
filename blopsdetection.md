Blops Detection

For Blops pr min (BPM) detection you can either use a MPU6050 sensor or a sound sensor lm939 to follow the acivity of released CO2.

The MPU6050 is soldered till ESP32 and can be used with both S-airlocks and the 3-peice-airlocks. It works by detect the small vibrartion an airlock makes, and hence, neeed some vibration-isolation as flamingo to work.
![diagram2_esp32](https://github.com/kbaggen/SPINDELMATE/assets/16992918/7c83d1a8-4c0a-4187-853c-b562b80e9360)

Or you can use lm393 sound sensor as below. The later fits perfectly into a S-airlock "head", and by adding a smal water ballon for moisture protection it give a pefect fit, and detects the sound when CO2 is released. To get best sound a small hole needs to be drilled into the S-airlock to equalize pressure. The sound sensor is prone till blow-off and ofcouse high sounds, and hence is best used with a blow-off system.

![buidling-sensor](https://github.com/kbaggen/SPINDELMATE/assets/16992918/9ecd153b-c536-4b11-9bb7-c5bcb28b7b20)



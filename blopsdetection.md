     BlopsDetect Info
     <img src='https://iblopper.bubble-logger.com/wp-content/uploads/2021/10/gif-1.gif' alt='' height="24%">
     For Blops pr min detection (BPM) you can either use a MPU6050 sensor as above and hence by vibration of the airlock follow the acivity of released CO2.<BR><br> Or you can use lm393 sound sensor as below. The later fits perfectly into a S-airlock "head", and by adding a smal water ballon for moisture protection it give a pefect fit, and detects the sound when CO2 is released. To get best sound a small hole needs to be drilled into the S-airlock to equalize pressure.
     <img src='https://iblopper.bubble-logger.com/wp-content/uploads/2023/05/buidling-sensor.png' alt='' height="21%">
     
     
    Selection/Sensitivity:
Please enter "1000" for Sound detection. For MPU6050 and hence vibration detrrection, please enter a number higher than 1, but please be aware this number also set the sensitivity of the MPU6050. From experiance and the used TicTax box a value of 4 is most suited, but you can adjust if you see to many or to little blops. For Sound Sensor the adjusment is done directly at the small potentimeter of the sensor.<b> TURN OFF?</b> To turn Blops detection off, please just enter "0". This will also remove the info/graph from the overwiev.
              
 <b>Diagram for Buidling (esp-wroom-32 devkit v1):</b>
     <img src='https://iblopper.bubble-logger.com/wp-content/uploads/2023/05/diagram2_esp32.png' alt='' height="21%">

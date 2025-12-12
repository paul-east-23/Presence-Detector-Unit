This my test of saving ESPHome yaml on Github and loading it into an ESP23C3 Zero.

The unit is a Presence / Detector Unit with an AHT20 temp/humidity and BH1750 illuminance sensor.

There is also going to be a JST connector to allow 2 additional inputs/outputs as well as either 5V out or 12V in to power the unit.

         5V    [USB]    21  
         GND            20  
         3V3            19  
 SDA     0              18  
 SCL     1              10  
 Rx/1020 2               9  
 TX      3               8  
 JST-Y   4               7  Jumper to LED
 JST-W   5               6  Jumper to LED

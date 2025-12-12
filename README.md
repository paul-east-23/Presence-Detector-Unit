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

Add the following to your ESPHome config

```
packages:
  # Onboard LED, switch to turn off indications
  base: 
    url: https://github.com/paul-east-23/Presence-Detector-Unit
    ref: main
    refresh: 0d
    file: unitbase.yaml
  
  # AHT20 and BH1750 sensors
  sensors: 
    url: https://github.com/paul-east-23/Presence-Detector-Unit
    ref: main
    refresh: 0d
    file: sensors.yaml
  
  # Select one depending on the module installed
  ld1020: 
    url: https://github.com/paul-east-23/Presence-Detector-Unit
    ref: main
    refresh: 0d
    file: ld1020.yaml
  
  #ld2420: 
  #  url: https://github.com/paul-east-23/Presence-Detector-Unit
  #  ref: main
  #  refresh: 0d
  #  file: ld2420.yaml
```

# Smart Airsoft Targets

This will eventually be a repository of all the design files and code for my smart airsoft target system.

I am making 16 200x200mm targets and 4 200x300mm targets.

Each target: 
- Is battery powered (2500mAh 18650)
- Ha    s 4 piezo electric discs to detect being shot( and potentially triangulate where it got shot for a more precise game mode)
- Has an esp8266 inside
- Communicates with a master ESP32 over ESP-NOW
- Has LEDs to indicate state (whether to shoot or not / how many shots left until target is considered hit / down)

I am also building a mega charging station for charging 10 at a time. Each target's charge module can take 2.1 Amps so its going to be quite a hefty charging station :/

## Decisions to make
- Double slit or single wide of LEDs

## Power calculations
LEDs: 50mA per LED
Battery: 2500mAh

10 LEDs (2 strips of 5 or one strip of 10):
2500/(40*10) = 6.25 Hours of runtime

12 LEDs (2 strips of 6 or 3 x4 grid):
2500/(40*12) = 5.20 Hours of runtime

14 LEDs (2 strips of 7):
2500/(40*14) = 4.46 Hours of runtime

15 LEDs (3x5 grid):
2500/(40*15) = 4.16 Hours of runtime

## LED Dimensions

12mm strip width

3 LEDs long: 23mm
4 LEDs long: 30mm
5 LEDs long: 36.5mm
6 LEDs long: 43.5mm
7 LEDs long: 50mm
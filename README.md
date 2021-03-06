# micropython-gy521
(!!! Unstable, WIP!!!)
Micropython library to interface with GY521 (Invensense MPU-6050 6-axis accel+gyro)

## Getting Started notes:
I needed to conda install virtualenv and cookiecutter in the root Conda env.
Probably useful in general, so they can be global.

## Plan:
* Make it work
* Make it as pythonic as possible
* Make it as async as possible
* Make it as light as possible

## Sources:
(https://github.com/larsks/py-mpu6050) for the idea.  No code reused.

(https://www.invensense.com/wp-content/uploads/2015/02/MPU-6000-Datasheet1.pdf)

(https://www.invensense.com/wp-content/uploads/2015/02/MPU-6000-Register-Map1.pdf)

Do I need to run with native code and the Invensense EmbeddedMotionDrive?
## CI Links
* (https://travis-ci.org/jpvlsmv/micropython-gy521) [![Build Status](https://travis-ci.org/jpvlsmv/micropython-gy521.svg?branch=master)](https://travis-ci.org/jpvlsmv/micropython-gy521)
* (https://readthedocs.org/projects/micropython-gy521/) [![Documentation Status](https://readthedocs.org/projects/micropython-gy521/badge/?version=latest)](http://micropython-gy521.readthedocs.io/en/latest/?badge=latest)
* (https://pyup.io/account/repos/github/jpvlsmv/micropython-gy521/) [![Updates](https://pyup.io/repos/github/jpvlsmv/micropython-gy521/shield.svg)](https://pyup.io/repos/github/jpvlsmv/micropython-gy521/)


### Some dev notes about my hardware:
```
Label GPIO || GPIO Label
  3V3      ||        Vin 
  GND      ||        GND
   TX    1 ||         EN
   RX    3 ||        RST
   D8   15 ||        3V3
   D7   13 ||        GND
   D6   12 ||    6   CLK
   D5   14 ||    7  MISO
  GND      ||   11    CS
  3V3      ||    8  MOSI
   D4    2 ||    9   
   D3    0 ||   10
   D2    4 ||   --
   D1    5 ||   --
   D0   16 ||  ADC
```

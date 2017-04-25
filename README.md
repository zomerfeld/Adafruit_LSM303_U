# Adafruit LSM303_U

A port to Particle of Adafruit's [LSM303DLHC Library](https://github.com/adafruit/Adafruit_LSM303DLHC). Ported on April 2017, tested on the Particle Photon. 

This driver is for the Adafruit LSM303 Breakout (http://www.adafruit.com/products/1120), and is based on Adafruit's Unified Sensor Library (Adafruit_Sensor).

## About the LSM303 ##

The LSM303 is a digital (I2C) accelerometer and digital compass (magnetometer).  The accelerometer allows you to measure acceleration or direction towards the center or the earth, and the magnetometer measure magnetic force, which is useful to detect magnetic north.

More information on the LSM303 can be found in the datasheet: http://www.adafruit.com/datasheets/LSM303DLHC.PDF

## What is the Adafruit Unified Sensor Library? ##

The Adafruit Unified Sensor Library (**Adafruit_Sensor**) provides a common interface and data type for any supported sensor.  It defines some basic information about the sensor (sensor limits, etc.), and returns standard SI units of a specific type and scale for each supported sensor type.

It provides a simple abstraction layer between your application and the actual sensor HW, allowing you to drop in any comparable sensor with only one or two lines of code to change in your project (essentially the constructor since the functions to read sensor data and get information about the sensor are defined in the base Adafruit_Sensor class).

This is imporant useful for two reasons:

1.) You can use the data right away because it's already converted to SI units that you understand and can compare, rather than meaningless values like 0..1023.

2.) Because SI units are standardised in the sensor library, you can also do quick sanity checks working with new sensors, or drop in any comparable sensor if you need better sensitivity or if a lower cost unit becomes available, etc. 

Light sensors will always report units in lux, gyroscopes will always report units in rad/s, etc. ... freeing you up to focus on the data, rather than digging through the datasheet to understand what the sensor's raw numbers really mean.

## About this Driver ##

Adafruit invests time and resources providing this open source code.  Please support Adafruit and open-source hardware by purchasing products from Adafruit!

Written by Kevin (KTOWN) Townsend for Adafruit Industries, ported by Noam Zomerfeld


## Wiring

The Photon use D0 for SDA and D1 for SCL, unlike other Arduinos.

Connect: 
- VIN to 3.3V (or 5v from VIN on the Photon, the LSM303DLHC is 5V tolerant)
- GND to GND
- SDA to D1
- SCL to D0

See the [examples](examples) folder for usage for the compass or the accelerometer.



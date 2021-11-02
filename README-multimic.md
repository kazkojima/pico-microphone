# Addendum for multiple SPH0641LU4H-1 microphones

The usmultimic branch is to add an experimental support for multiple SPH0641LU4H-1 ultrasonic microphones. Currently number of microphone has to be hardcorded with .define directive in pdm_microphone.pio.
```
.define PUBLIC NUM_DATA_PINS 2
```
will be for 2 microphones. Also you need to multiply decimation value by NUM_DATA_PINS.
```
cmake .. -DPICO_BOARD=pico -DUSMIC=y -DSAMPR=72 -DDECIM=128
```
will give 72kHz sampling rate and 4.608MHz(=72kHz*128/2) PDM clock.

The default sample rate is 144kHz for usmic which is hard coded in the top CMakefile.txt.

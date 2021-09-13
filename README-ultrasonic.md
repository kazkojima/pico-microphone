# Addendum for Ultrasonic microphone SPH0641LU4H-1

The usmic branch is to add an experimental support for SPH0641LU4H-1 ultrasonic microphone. To enable SPH0641LU4H-1 support, add -DUSMIC option when running cmake.

```
cmake .. -DPICO_BOARD=pico -DUSMIC=y
```
instead of the plain
```
cmake .. -DPICO_BOARD=pico
```
in the build procedure. See README.md for detail.

The default sample rate is 144kHz for usmic which is hard coded in the top CMakefile.txt.

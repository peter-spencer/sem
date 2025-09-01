# N80HD01

## Regulated power supply and high-voltage drive

This board provides regulated power supplies for the high-voltage drive circuits and also includes part of the high-voltage drive circuit for the CRT displays and the Scintillator detector.

## Power supply specifications

|Voltage|Current|Purpose|Notes|
|---|---|---|---|
|+15 Volts|Output transistor 3.5 Amps emitter current|Positive rail for HV drives| |
|-15 Volts|Output transistor 3.3 Amps emitter current|Negative rail for HV drives| |
|+70 Volts|2 Amps (fused F2-1,F2-2)|HV drive power|75 Volts on some schematics|

## Issues, fixes and upgrades

### +70 Volt power supply

The +70 Volt power supply failed after the problems with the high-voltage (oil) unit and it was left outputting the ~90 Volts unregulated supply voltage.

The simulations showed that there is a design issue with the output transistor triplet: Under heavier loads, the collector current in middle transistor of the triplet (TR6) can rise to be equal to the collector current of the final transistor (off-board in the dry high voltage unit). TR6 is not rated for these currents and has no provision for dissipating the Watts of heat generated.

Overloading of TR6 will occur before either of the 1 Amp fuses would normally blow and this is probably what caused the failures of TR4,5,6 and ZD11.

The solution I am going to try is to replace the output transistor with a Darlington NPN that is rated to handle the 90 Volt unregulated supply voltage with a reasonable margin for error. TR5 and TR6 will be bypassed and removed.

In simulation this seems to completely resolve the issues with overloading before the fuses could blow.

### ±15 Volt power supply

No problems with this supply have been found yet and the simulation suggests that the current circuit works well enough. Modern regulator chips such as a 7815 and 7915 pair will probably perform at least as well if not better and so should be considered as a replacement if this supply fails in future.

### High voltage driver for Scintillator and CRTs

I suspect that this may have been damaged by the +70V supply failure: **To be determined**.
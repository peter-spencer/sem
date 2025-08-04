# High Voltage System

Working out how the acceleration voltage and filament drive work in detail.

The KiCad schematic file contains all the circuits directly involved in controlling the Acceleration Voltage and Filament Current, including the read-out of Emission Current.

The LTSpice simulation file contains a simplified model of the oscillator and a part of the driver circuit that I made to check that I had correctly understood them.

I've included detail from the front-panel switches through to the emission current read-out to fully understand how the complete system functions.

The oscillator is sensitive to the selection of its Op-Amp component: The schematics show a 709 Op-Amp which is very obsolete and so it's not clear how this could be replaced if it was faulty.
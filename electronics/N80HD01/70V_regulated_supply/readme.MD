# 70 Volt regulated supply simulation

This is a SPICE simulation of the +70 Volt regulated supply for troubleshooting purposes.

It has been able to diagnose that TR6 can be overloaded and burn-out before the protection fuses (2x 1 Amp in the dry high voltage unit) blow.

Replacing the off-board output transistor with a Darlington NPN rated for the full load, and bypassing TR5 and TR6, appears to be good solution.
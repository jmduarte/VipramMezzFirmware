VipramMezzFirmware
==================
Hooking up the mezannine:
 * Plug in the power supply to the mezzanine
 * Plug in Ethernet chord from the back of the computer into mezzanine
 * Plug JTAG into mezannine, and the USB end into the computer
Power Supply:
 * Turn on the 2nd (right side) power supply. It should have the following settings:
```
Out 1: ~3.5 V
Out 2: ~12 V
 ```
 * Press shift and then press CURRENT ↑ / VOLTS ↑ to switch between Out 1 / Out 2
 * Press ON/OFF to toggle power current to mezzanine. If set up properly, green light should be on underneath
Terminal: (Set up environment)
 * Type the following into the terminal:
```bash
source /home/ntran/Documents/VipramTesting2015/TestingPacakge_Aug26/setupHAL.sh
source /home/ntran/Documents/VipramTesting2015/VipramMezzFirmware/mymezz1/setup_environment.sh
analyzer &
``` 
* This will set up the environment and launch ChipScope PRO Analyzer.

Chip Scope PRO Analyzer:
 * Press "OK" twice
 * Go to JTAG Chain in the toolbar and select Xlink Platform USB Cable
 * Right click DEV:0 MyDeviceO under New Project > JTAG Chain
 * Choose "Configure"
 * Press "Select New File"
 * Choose executable file location (file:  /home/ntran/Documents/top.bit)
 * Press "OK"
 * Wait for programming to complete. Progress bar in bottom-right corner

# AT28C256 EEPROM flasher
Made with the Arduino Mega.
To use, clone the repo and upload the .ino file to the arduino mega.

Then run the python script to upload your binary file to the arduino (which will then flash it to the EEPROM).

`Usage: python eeprom.py [R/W] [filename] [port]`

For example:

`python eeprom.py W ./rom.bin /dev/ttyACM0`

By default, the arduino program uses pins 22-52 (even-numbered) as the pins for the address bus (22->A0, 24->A1, 26->A2 etc.), and the odd-numbered pins from 31-45 as the pins for the data bus (31->I/O0, 33->I/O1, 35->I/O2 etc.). However, these pin numbers can be reconfigured by simply changing the values in the two arrays, "address_bus_pins" and "data_bus_pins."
# wireshark-cc2531

Wireshark extcap interface for the Texas Instruments CC2531 USB dongle with the factory-installed IEEE 802.15.4 packet sniffer firmware.

![Screenshot](screenshot.png)

## GNU/Linux

1. Compile the cc2531.c extcap program:
  * sh build.sh
2. Copy the resulting cc2531 executable to the wireshark extcap directory with permissions to read-write the /dev/bus/usb/XXX/YYY device node of the TI CC2531 USB dongle. One way to do this is:
  * sudo install -m 2755 cc2531 /usr/lib/x86_64-linux-gnu/wireshark/extcap/cc2531
3. Run wireshark, select the "TI CC2531 802.15.4 packet sniffer" capture interface, choose the IEEE 802.15.4 2.4GHz radio channel to capture (11 to 26) and start capturing.

## Windows

1. Copy the pre-compiled cc2531.exe extcap program to the wireshark extcap directory, typically C:\Program Files\Wireshark\extcap (or run build.bat to compile it yourself).
2. Plug in your TI CC2531 USB dongle to your computer
3. Use [Zadig](https://zadig.akeo.ie/) to configure windows to use the WinUSB driver with the "CC2531 USB Dongle" device. (See https://learn.microsoft.com/en-us/windows-hardware/drivers/usbcon/winusb-installation for more info.)
3. Run wireshark, select the "TI CC2531 802.15.4 packet sniffer" capture interface, choose the IEEE 802.15.4 2.4GHz radio channel to capture (11 to 26) and start capturing.

## License

This program is free software; you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation; either version 2 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License in the LICENSE file for more details.

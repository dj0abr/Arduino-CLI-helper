# Arduino-CLI-helper
Arduino CLI helper scripts for Linux make using Arduino CLI very simple and convenient
# why Arduino CLI ?
while the Arduino framework is a very powerful and simple to use framework, the Arduino GUI is very limited, even the newest versions.
I prefer to edit my code with VS-code and compile it in the command line using Arduino-CLI (CLI = command line interface, which is Arduino without GUI)
# what are these scripts doing ?
## install_arduino-cli:
this script is used to install the complete Arduino-CLI framework required for ESP32 applications.
## ard:
this script contains all commands which are used to:
clear the complete flash memory, write the bootloader, write the partition table, flash an application firmware, flash littleFS data. Flashing the firmware and littleFS data can be done via USB or OTA (Wifi). Execute ./ard to get a list of commands. 
These settings should be adapted to your requirements:

BOARD="esp32:esp32:esp32" (you can use that as it is, works with most ESP32 boards)

PARTITION="default" (you can use that as it is, works with most ESP32 boards)

BAUDRATE=921600 (you can use that as it is, works with most ESP32 boards. If you flash via a virtual machine or on a slow PC, reduce this value to e.g. 115200)

USBPORT="/dev/ttyUSB0" (the serial port, can be left unchanged in most cases)

IPADDRESS="192.168.10.83" (only for OTA: the IP address of your ESP32 board)


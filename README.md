# Wifi Penetration Tool ESP32
## Purpose
This is for my final project it follows Risineks documentation and allows the esp32 to become a wifi penetration tool.
### Equipment
1. ESP32
2. Micro USB
#### Documentation
1. (https://github.com/risinek/esp32-wifi-penetration-tool)
2. (https://www.youtube.com/watch?v=YjekZXoy91Y)
##### Steps
1. I downloaded Risinek's project zip file and unzipped it 
2. Install Python 
3. pip install esptool on python 
4. Open cmd and run this while the esp32 is connected make sure to change what's in between -p and -b to what com port is being used
5. esptool.py -p /dev/ttyS5 -b 115200 --after hard_reset write_flash --flash_mode dio --flash_freq 40m --flash_size detect 0x8000 build/partition_table/partition-table.bin 0x1000 build/bootloader/bootloader.bin 0x10000 build/esp32-wifi-penetration-tool.bin
6. make sure the directory is correct 
7. It is now installed 
8. Open up network connections and connect to ManagementAP the password is mgmtadmin 
9. The ESP32 now acts as a router for testing you would need to go to 192.168.4.1 
10. Tick which wifi connection you want to test and what attack you want to carry out and start during its attack time you are unable to connect to the esp
###### Problems 
One of the problems I had was the pip install of the esp32 was not working i just had to change an option in uninstall or change program go to python and modify and check off add python to environment variables. 
the second issue I had was the code I had to remove the .py from esptool for it to start installing to the ESP 

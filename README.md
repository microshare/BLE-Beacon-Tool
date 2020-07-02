# BLE-Beacon-Tool

## Requirements
Raspberry Pi3 Model B+
https://www.raspberrypi.org/products/raspberry-pi-3-model-b-plus/

Debian Buster with Raspberry Pi Desktop</br>
Version: February 2020</br>
Release date: 2020-02-12</br>
Kernel version: 4.19</br>
Size: 2985 MB</br>
SHA-256: e9931ba401241281f7c2d32b703227acabb054159792abdbd3f2d6ce09454e20

https://downloads.raspberrypi.org/rpd_x86/images/rpd_x86-2020-02-14/

## Quick Start Raspberry Pi3 Model B+

Please see the below instructions on how to download the Buster image to the Raspberry Pi
https://www.raspberrypi.org/downloads/

## Quick Start BLE-Beacon-Tool

It is easy to setup the dependencies on the Raspberry Pi3 Model B+</br>
This takes approximately 1 hour to download and install dependencies.

1. Open the terminal, type and execute the command:

>> git clone  https://github.com/microshare/BLE-Beacon-Tool.git

2. On the terminal, type and execute the command:

>> sudo sh BLE-Beacon-Tool/setup_environment.sh

3. We will then need to create a MAC Address list of our BLE-Beacon's.

4. Send the MAC Address list to your Microshare contact, the BLE-Beacon pairing codes will be generated.

5. Upon receipt of the MAC_Address_Pairing.txt from Microshare, we are then ready to run automate.py

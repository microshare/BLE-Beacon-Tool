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

### Headless Setup (Optional)

### Enable SSH on Raspberry Pi Headless

1. After the image succesfully imaged to the SD Card, open the SD Card in file explorer and simply create a file named ssh in the boot partition (the file does not expect any extension).

### Set up a static ip for your Raspberry Pi Headless

1. In order to know the ip that the Raspberry Pi will take, we will give it a static ip. For this we will modify the file dhcpd.conf located in the /etc/folder
2. Edit the file with your text editor e.g. vim or nano. 
3. Once in the file, go to the last line and add the following content:

eth0 
static ip_address = 192.168.1.100 / 24 
static routers = 192.168.1.1 
static domain_name_servers = 192.168.1.1

### Connect the Raspberry Pi to your Wi-Fi router

1. In order to configure the Wi-Fi connection when starting the Pi, we will create the wpa_supplicant.conf file in the boot partition.
2. In the ssid line , you will replace YourRouterName with the name of your box, for example , Livebox-5678. 
3. For the psk field , this corresponds to the security code of your box, so replace YourRouterSecurityCode by the key of your box
4. The file must contains the following lines:

country=fr
update_config=1
ctrl_interface=/var/run/wpa_supplicant

network={
 scan_ssid=1
 ssid="YourRouterName"
 psk="YourRouterSecurityCode"
}

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

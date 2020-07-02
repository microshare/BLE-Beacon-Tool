# Useful Commands

### hciconfig

* hciconfig hci0 up
* hciconfig hci0 down

### hcitool

* sudo hcitool lescan
* sudo hcitool lecc AC:23:3F:66:47:7D

### gatttool

* sudo gatttool -t random -b AC:23:3F:66:47:7D --char-write-req -a 0x5001 -n 0x70110204 --listen
* sudo hcitool lescan | grep KLK
* sudo gatttool -t random -b AC:23:3F:66:47:7D -I

### bluetoothctl

* power off
* power on
* agent on
* scan on
* scan off
* info <MA:C0:0A:DD:RE:SS>

### Configure bluetooth.service experimental mode

1. sudo nano /lib/systemd/system/bluetooth.service
2. Append --experimental
   Before:
   ExecStart=/usr/lib/bluetooth/bluetoothd
   After:
   ExecStart=/usr/lib/bluetooth/bluetoothd --experimental

### Terminal path to success
* sudo hcitool lecc MA:C0:0A:DD:RE:SS
* bluetoothctl
* pair
* 123456
* info
* select-attribute c5cc5000-127f-45ac-b0fc-7e46c3591334
* write 0x0070
* write 0x0011
* write 0x0002
* write 0x0004

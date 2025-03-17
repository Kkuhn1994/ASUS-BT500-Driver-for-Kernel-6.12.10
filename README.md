# ASUS-BT500-Driver-for-Kernel-6.12.10
i didnt find a working driver for my kernel so i made some changes


sudo make install INTERFACE=usb
sudo modprobe rtk_btusb

see if adapter is recognized:
lsmod | grep rtk_btusb

hciconfig -a
sudo systemctl start bluetooth
sudo hciconfig hci0 up




should be working now try findind and connecting device 
i had problem with connecting 2nd device over UI but it works fine with the CLI

bluetoothctl

scan on
connect XX:XX:XX:XX:XX:XX




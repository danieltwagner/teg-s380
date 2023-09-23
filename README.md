# Trendnet TEG-S380 V1.0R
A fanless 8 port 2.5G switch
- Flash: 2MB, Macronix MX25L1606E 3.3V
- UART pin order: VCC (arrow), TX, RX, GND

Getting a shell:
```
pyserial-miniterm --eol LF --raw /dev/cu.usbserial-* 115200 | tee out.txt
```

Flash dump:
```
sudo apt install libusb-1.0-0-dev
git clone https://github.com/setarcos/ch341prog.git
cd ch341prog && make
./ch341prog -i
./ch341prog -r flash.bin
```

## Links
- Version v1.0R https://www.trendnet.com/products/2-5g-switch/8-port-unmanaged-2-5g-switch-TEG-S380 supports 1G and 2.5G speeds
- Version v1.xR https://www.trendnet.com/products/2-5g-switch/8-port-unmanaged-2-5g-switch-TEG-S380-v1.1 adds 10/100 mbit
- https://www.servethehome.com/trendnet-teg-s380-8-port-2-5gbe-switch-review/
- https://forum.openwrt.org/t/support-for-rtl838x-based-managed-switches/57875/2392
- https://forum.openwrt.org/t/support-for-rtl838x-based-managed-switches/57875/2432
- https://pastebin.com/1UJca8ma

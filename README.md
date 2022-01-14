# R29-MXQ-LP3-V2.3-00908
RK3228(A) TV box teardown

Andoid 10.1 (real 7.X)

Kernel 3.10.104

Flash / RAM (probely fake)
```
Flash ID: 45 4d 4d 43 20
Manufactur SAMSUNG
Flash Size 7472MB
Total sectors: 0xe98000
Block size: 512KB
Page size: 2KB
ECC bits: 0
Access time: 40
Flash CS: 0
```
Installing  SSH helper and terminat in android and using this for duning the device tree:
```
tar -zcvf  device.tar.gz /sys/firmware/devicetree/base/
```
No comport pads found only 2 bads for bootig in mask rom (is near one of the not mounted maory chips see photo).

ARMBian and libreelec is the HDMI not working.
libreelec its possible adding "ssh" and can conecting with SSH.

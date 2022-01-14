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
No comport pads found only 2 pads for bootig in mask rom (is near one of the not mounted meory chips see photo) and on the under side near the CPU but not knowing what its for. I think the comport is on the SD-card conection but have not testing it.
![MASK-rom](RK3228A2.jpg)
![ComP?](RK3228B3.jpg)
![SD-Card](RK3228A4.jpg)
I think (= have not testing) its the 4 contact from right and its pinnumber 5 then 9 is on the phased side and befor number 1 and is SCLK that is logic.

ARMBian and libreelec is booting OKbut the HDMI not working.
libreelec its possible adding "ssh" and can conecting with SSH.
DMESG from boot of libreelec with rk3228a-box.dtb as config (no WiFi and no critical errors = very OK).


Trying dunping with RK-dump but not working also with older derivers installed.
RK_Android_Tool i can dooing dumps but i is 110% they is OK.
Parameters looks being red OK and i have making it more times.
```
PARM  FIRMWARE_VER:7.0.0
MACHINE_MODEL: hx322x_box
MACHINE_ID:007
MANUFACTURER:RK30SDK
MAGIC: 0x5041524B
ATAG: 0x60000800
MACHINE: 3228
CHECK_MASK: 0x80
KERNEL_IMG: 0x60408000
#RECOVER_KEY: 1,1,0,20,0 
CMDLINE:console=ttyFIQ0 androidboot.selinux=permissive androidboot.hardware=rk30board androidboot.console=ttyFIQ0 init=/init mtdparts=rk29xxnand:0x00002000@0x00002000(uboot),0x00004000@0x00004000(trust),0x00002000@0x00008000(misc),0x00000800@0x0000A000(baseparamer),0x00007800@0x0000A800(resource),0x00006000@0x00012000(kernel),0x00006000@0x00018000(boot),0x00010000@0x0001E000(recovery),0x00020000@0x0002E000(backup),0x00040000@0x0004E000(cache),0x00008000@0x0008E000(metadata),0x00002000@0x00096000(kpanic),0x00400000@0x00098000(system),-@0x00498000(userdata)
»Ü‰¤                                                                                                                                                                                                                                                   
```
Shall testing dumping the flash from Linux.

Thinkin is i dont need the internal flash its also possible using SD-card and running ARMBian and if can patching one image file with libreelec boot and ARMBrian system it wold being great for running docker with RTL-433 and other good things.


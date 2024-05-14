# 3516AIO
My Hi3516EV200+IMX307+RTL8731BU All-in-One FPV Camera   

Bilibili video [here](https://www.bilibili.com/video/BV1S1421q7vK)   

OSHWHub link [here](https://oshwhub.com/libc0607/hi3516ev200_imx307_rtl8731bu_aio_v1p1_rel)    
This is an OSHWHub mirror. Always check the link for updates.  

![image](https://github.com/libc0607/3516AIO/assets/8705034/8d6b80cd-e037-4a49-a454-30b37f5653d1)  
![image](https://github.com/libc0607/3516AIO/assets/8705034/094ace97-0ef7-445b-8a8a-ef2a47d08bcd)  


## Hardware Feature  
 - Hi3516EV200/GK7205V200, OpenIPC supported 
 - IMX307 Sensor, 20mm lens mount (the surveillance camera standard)
 - RTL8731BU ([BL-M8731BU*](https://www.b-link.net.cn/product_34_287.html) module), 2.4GHz/5GHz injection, 20dBm+ TX, LDPC  
 - 1.27mm header for ext. board, including I2C\*1/UART\*3/SDCard\*1/Ethernet/ADC\*1
 - 2S battery input (but it will work under 1S/3S with slightly modifications)
 - Ultra-light, <9g weight (including lens, mount, heat sink, and antenna; See image below)
 - ~3W typical electrical power consumption

PCB: 4L, 0.8mm thickness. Should not concern the impedance because the total length of each MIPI trace is even less than (wavelength/20).  

![image](https://github.com/libc0607/3516AIO/assets/8705034/d6a3f5d5-95af-4250-b877-33910914489b)  
![image](https://github.com/libc0607/3516AIO/assets/8705034/b3dae2d0-eda4-4116-a1a5-2090639dbe86)  


## Software 
It runs OpenIPC. Compiling: 
 - Hi3516EV200/GK7205V200 target
 - set RTL8733BU driver = y in board config
 - set OpenIPC Variant = "fpv" in board config
 - set CONFIG_WIRELESS_EXT=y in kernel config
 - set WIRELESS_EXT in kernel source net/wireless/Kconfig  

![image](https://github.com/libc0607/3516AIO/assets/8705034/31d06d50-fee9-4d1c-b84c-89a3564d38f8)


## Files here 
[ProProject_3516_307_8731_devboard_V1.1_2024-05-14.epro](https://github.com/libc0607/3516AIO/blob/main/ProProject_3516_307_8731_devboard_V1.1_2024-05-14.epro): EasyEDA (LCEDA) Project file, including schematic and PCB  
[3516aiov1p0_v1.STL](https://github.com/libc0607/3516AIO/blob/main/3516aiov1p0_v1.STL): A holder compatible with a 1/4" screw. Use with a 1/4" x 10mm(height) x 8mm(diameter) knurling nut

## License 
[CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)   

This is only a low-cost prototype of validating the idea of how small the size we can fit an OpenIPC-runnable All-in-One hardware into.  
Personally speaking, I prioritize its cost and size over its encoding performance. So -- I'm gonna keep it open-sourced, and not for commercial use.  


# MH1905 EVB LVGL demo

This demo source code is based on LVGL's Github codes. The music demo and widget demo is available to work on MH1905-EVB.

 [YouTube demo][link-youtube]

## 🧰Required tools
1. Ubuntu OS - 22.04
2. MH1905_LVGL file - Download directly from github
3. [Toolchain file][link-toolchain]
4. MH1905 EVB

## Procedures
1. Required package in Ubuntu OS - flex, bison, gcc and make
2. Put your toolchain file inside the MH1905_LVGL file
3. Unpack tar file in toolchain
```
tar -xvf arm-linux-gnueabihf-7.3.tar
``` 
3. Export file using the toolchain

```
export CC==toolchain/arm-linux-gnueabihf-7.3/bin/arm-linux-gnueabihf-gcc
export AS==toolchain/arm-linux-gnueabihf-7.3/bin/arm-linux-gnueabihf-gcc
```

4. Modify your main.c file to your wanted LVGL demo and save your settings 
```C
 /*Create a Demo, select your own demo*/
    //lv_demo_widgets();
    lv_demo_music();
    //lv_demo_benchmark();
```
5. Make clean and Make file

```
make clean && make
```
6. Find the demo script and save it to MH1905 EVB

7. Load the demo


[link-toolchain]: https://drive.google.com/file/d/1gXdgwlnbOotSAJcPmpOhN2TLddEUrL7T/view?usp=drive_link
[link-youtube]: https://youtu.be/qqwIV1IWNEY

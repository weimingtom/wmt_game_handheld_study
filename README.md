# wmt_game_handheld_study
My game handheld study

## TODO  
```

showbmp_luckfox_v5_1.44_bmp.zip

芒果派mqpro
search mangopi-sbc_Tina-Linux-main.zip

https://github.com/pangweiwei/slua



esp32one+gamepi20
ips2_0_esp32_2_esp32one_gamepi20_v1_wifi_no_auto_shutdown.7z
ips2_0_esp32_esp32one_gamepi20_v5_wifi_no_auto_shutdown.7z


freej2me
https://ashiningray.github.io/freej2me/
https://github.com/MiyooMini
https://github.com/TriForceX/MiyooCFW/wiki/穿越操作系统迷雾


atj2273s

M3掌机

小志掌机屏幕并口
lcd_28_16_v1.7z
用中景园STM32F103RCT6开发板（可能已经停产了）驱动小志掌机30针并口屏，大致成功了，效果如下，线多。并口在文档中称为I8080 16bit（或者叫MCU 8080），通过3个脚的电平区分模式（并口16，并口8或者4SPI）。注意16深的数据线不能接错，例如一个叫PB2，应该接在BOOT1上，如果接在PD2上就出问题，另外颜色有问题，可能高低位反转了，中景园提供的驱动代码可能不完全兼容这个屏。待考
lcd_28_16_v2_success_invon.7z


https://www.cnblogs.com/liangliangge/p/12626248.html
getevent -lp
getevent -lt
sendevent
https://bbs.16rd.com/thread-581476-1-1.html
https://d1.docs.aw-ol.com/strong/strong_1display/


rp2040_pizero_v1_LCDTestV2_success_gamepi20.7z
rp2040_pizero_v2_dino.7z

小志掌机
work_getevent_v2.7z


小志掌机的qt和lvgl代码未上传网盘
*
https://bbs.aw-ol.com/topic/3751/全开源-小志掌機gaviar-handheld-资料汇总/9
run rom : tina_d1s-gaviarhandhelda_uart4.img
xiaozhi_256m.7z
*
graywin, SDL1
SDL-1.2.15_makefile_build.tar.gz
SDL-1.2.15_makefile_xiaozhi_v1.tar.gz
*
fv, for replacing fbv witch not work
fvjpeg6b_v4_xiaozhi.tar.gz
* lvgl lv_port_linux_frame_buffer_xiaozhi_v1.tar.gz
*
qt4 nes
qt4-nes_v5_xiaozhi.tar.gz
qt4-nes_v6_boot.tar.gz qt-everywhere-opensource-src-4.8.6_riscv64.tar.gz


用stm32驱动小志掌机并口屏的接线方法，见
lcd_28_16_v2_success_invon.7z
https://bbs.aw-ol.com/topic/3751/全开源-小志掌機gaviar-handheld-资料汇总
（转接板是31-x）排线次序<->功能<->stm32
1<->GND,2<->3.3V
3<->RST<->PA4,4<->CS<->PA0
5<->RS<->PA1,6<->WR<->PA2
7<->RD<->PA3,8<->NC
9<->D3B<->PB0,10<->D4B<->PB1
11<->D5B<->PB2（BOOT1）,12<->D6B<->PB3
13<->D7B<->PB4,14<->D10G<->PB5
15<->D11G<->PB6,16<->D12G<->PB7
17<->D14G<->PB8,18<->D15G<->PB9
19<->D18G<->PB10,20<->D19R<->PB11
21<->D20R<->PB12,22<->D21R<->PB13
23<->D22R<->PB14,24<->D23R<->PB15
25<->3.3V?,26<->GND
27<->GND?,28<->LEDA+<->PA5
29<->LEDK-<->GND,30<->GND
数字跟实际是反过来，例如1实际对应转接板的30
stm32的pb2对应开发板上的BOOT1，不是PD2

de2 uclinux

树莓派按键输入
https://www.waveshare.net/study/article-602-1.html


小志掌机，按键输入成功
qt4-nes_v12_button_input_success.tar.gz
qt-everywhere-opensource-src-4.8.6_xiaozhi_v2.tar.gz
小志掌机研究。由于Qt4在小志掌机上的按键键码是乱的，我的想法是把evtest缩小版代码整个嵌入到用qt nes代码中，通过Qt线程启动，如果用Windows编译大概就是如下效果——当然只能模拟编译，效果要需要试验。我甚至看到有人用Qt网络库去读取linux input event设备事件，例如这篇《Qt之 读取 /dev/input/event*设备 并解析》，不过这篇是触摸屏输入

ddz
https://gitee.com/subingwen/landlords

研究gpicase
https://sirius10.net/Games/Akane.php
https://sirius10.net/RaspberryPi/ONScripter.html
树莓派编译
https://sirius10.net/Games/Bless.php

dpi24
https://www.raspberrypi.com/documentation/computers/raspberry-pi.html
复古旗应该是通过DPI24格式去显示，占用24脚之中的18脚（RGB666），详细见这篇《盘点那些树莓派与显示屏的连接方式》，DPI是Parallel Display Interface的缩写，可能对应panel-dpi这个驱动——简单来说就是跟SPI屏的驱动不一样，详细见文档：www.raspberrypi.com/documentation/computers/raspberry-pi.html
https://github.com/ian57/pwm-audio-pizero-gpicase
https://github.com/ian57/dpi-pizero-gpicase
https://zhuanlan.zhihu.com/p/353402654?utm_id=0
https://zhuanlan.zhihu.com/p/662096549?utm_id=0
https://retroflag.com/GPi-CASE.html
https://support.retroflag.com
话说树莓派的硬件文档很长，而DPI24这种显示总线怎么看上去那么像RGB并口屏幕（可能一样，少了背光BL，仅保留DE,VSYNC,HSYNC,CLK四个控制脚，文档是PCLK,DE,LCD_VSYNC,LCD_HSYNC）不过可以配置成不同的，例如RGB666，会忽略掉一些脚），从某种意义上可以复刻NES了（逃），至少颜色上是兼容的（逃）

小志掌机研究。这个研究快接近尾声了，至少今年应该不会继续研究，音频输出功能以后再说。关于GamePi20的声音输出，虽然相关的资料很少，但我觉得可能和GamePi15和gpicase是类似的，而这两个有一些资料显示声音输出的原理，所以下一年可能会研究，或者等我了解得比较多有把握再研究声音问题
qt4-nes_v2_rpi_final_success.tar.gz
raspberrypi_tools-master.zip
2018-04-18-raspbian-stretch-lite.zip

还差上传树莓派zero的qt4源码修改版
qt-everywhere-opensource-src-4.8.6_gamepi20_v1.tar.gz
```

## Gaviar-Handheld, 小志掌機, 小志掌机 (xiaozhi), Allwinner D1s    
* https://bbs.aw-ol.com/topic/3751/全开源-小志掌機gaviar-handheld-资料汇总/9  
run rom :
tina_d1s-gaviarhandhelda_uart4.img  
xiaozhi_256m.7z  

* graywin, SDL1  
SDL-1.2.15_makefile_build.tar.gz  
SDL-1.2.15_makefile_xiaozhi_v1.tar.gz    

* fv, for replacing fbv witch not work    
fvjpeg6b_v4_xiaozhi.tar.gz  

* lvgl
lv_port_linux_frame_buffer_xiaozhi_v1.tar.gz

* qt4 nes  
qt4-nes_v5_xiaozhi.tar.gz  
qt4-nes_v6_boot.tar.gz
qt-everywhere-opensource-src-4.8.6_riscv64.tar.gz  

* LEDC
```
小志掌机研究，今天来看看怎么控制左上角的彩灯，简单说就是把0到255之间的数输出到
/sys/class/leds/sunxi_led0r/brightness
（可能是sunxi_led0r，sunxi_led0g和sunxi_led0b三种颜色，0表示关闭）。
我是怎么知道的呢，其实看dts设备树源码，知道PE5是控制WS2812C-2020-V1彩灯，
驱动是LEDC，然后在文档《D1s
开发板使用简介》中查到LEDC的用法。由于树莓派没有这种玩法，
所以gamepi20忽略研究这个彩灯
```

* st7789v i8080 tft
```
关于小志掌机i8080 16模式屏幕的反色问题，很简单，找一段反色代码（搜索ST7735_INVON或者ST7789_INVON）
加入进去即可，例如这样（不需要输出DATA数据线，用delay代替）：
//ST7789_COLMOD=03a, ST7735_INVON=0x21 
LCD_WR_REG(0x21);
delay_ms(100); //Delay 120ms
然后颜色就正常了（st7789会帮忙自动反色），具体效果晚上给出
```

* UART
```
小志掌机研究。可以确定，如果不改设备树的话，提供的固件接usb键盘和鼠标是看不到动态event设备的，除非改设备树。
另外我焊接上了串口，串口从左到右丝印的TRG实际上是RTG，或者理解成接调试器的TRG，最左的方形焊盘不是地线。
我犯了个错误，我把调试器的地线接到开发板串口的R，结果串口居然也可以正常输出内容，但输入会无反应，
如果发现串口输入没反应，则有可能地线接错了，不一定是T线接错
```

* input, evtest, getevent
```
小志掌机研究。我测试过树莓派zero+GamePi20，可以成功编译和运行getevent（tina版，-lt参数）
和evtest（buildroot版），完全没问题，
只不过不能获取GamePi20的按键输入事件，因为设备树没有（但sysfs可能可以）。如此我想起其实存在第三个问题，
我可以用usb设备去取代手柄按键，但usb设备存在第三个问题，它是动态分配/dev/input/eventN的，
除非我可以在LVGL和Qt4中动态判断出哪个event设备从而获取键盘或者鼠标输入，
这方面LVGL可能做得不太好（都是固定的），Qt4也差不多。

总体来说关于小志掌机和GamePi20的输入功能，现在有三个问题待解决：
（1）如何简化getevent和evtest的按键鼠标输入代码且嵌入到模拟器代码中
（2）如何通过按键模拟轨迹球鼠标
（3）如何动态适配usb设备文件，从而自动适配usb鼠标和usb键盘
（树莓派zero应该可以，但小志掌机仍不确定是否可以接入usb鼠标键盘）

小志掌机研究。我用自带的evtest测试，对应snes手柄按键如下获得的键码和实体按钮对应关系如下。
你会发现设备树的标签名写错了，但我看过跟针脚名的对应是没错的，
我倾向于用snes的键名（即橙色列那个表），
我只要写一个程序读取/dev/input/event1的键码即可知道对应的键名（根据图一） ​​​

小志掌机研究。为什么要研究getevent和evtest呢？因为跟tft lcd输出类似，按键输入也可以分两种，
一种是通过gpio做（例如sysfs或者mmap），另一种是通过驱动实现，把gpio操作放在内核态。
用哪一种取决于设备树，但一旦设备树占用了，就有可能无法用gpio做按键输入了。
目前的情况是，小志掌机固件我没实际编译过（树莓派zero也是），
所以小志掌机固件的设备树（gpio-keys）限制了一定要类似于getevent或者evtest的做法，
通过设备驱动读取，而树莓派zero则没有这个限制，应该可以用gpio（例如wiringpi方式读入）。
我打算下一步研究怎么简化evtest的代码，看能否得到一个最小读取按键代码；
而对树莓派zero也做类似的工作

我比较一下小志掌机源码包的evtest和getevent，结论如下。
一、evtest和getevent的区别：
（1）evtest是buildroot的一个包，可能来源于gitlab或者gh。buildroot的补丁似乎可以忽略，
改动不大。evtest也是apt的一个包，可以通过apt安装到树莓派上
（2）getevent是tina的一个包（utils下，tina是来源于openwrt），来源于android的测试工具箱。
在source.android文档中有介绍。gh上也有人把它移植到ubuntu下。
二、两者的联系：代码量似乎相当都是1300多行，getevent分出头文件，evtest是单个c文件。
所以我怀疑本质上可能是相同的，都是根据几组标签常量数组来输出事件标签

小志掌机研究，我准备研究按键输入，目前有这几种可能的办法读取按键输入：
getevent（支持linux和android），evtest（支持linux），SDL（基于Linux），
lvgl（基于Linux），嵌入式Qt4（基于Linux），纯event方式读，gpio按键。
之所以这么麻烦是因为按键输入不一定只有高低电平，可能还需要模拟鼠标或触摸，
还可能出现ADC问题
```

* keycode  
```
evtest, /dev/input/event1
/dev/input/event0:      sunxi-gpadc0
/dev/input/event1:      gpio-keys
Select the device event number [0-1]: 1
1
Input driver version is 1.0.1
Input device ID: bus 0x19 vendor 0x1 product 0x1 version 0x100
Input device name: "gpio-keys"
Supported events:
  Event type 0 (EV_SYN)
  Event type 1 (EV_KEY)
UP, PE0,  左上：type 1 (EV_KEY), code 114 (KEY_VOLUMEDOWN), value 1->0
DOWN, PE7, 左下：type 1 (EV_KEY), code 115 (KEY_VOLUMEUP), value 1
LEFT: PE6, 左左：type 1 (EV_KEY), code 116 (KEY_POWER), value 1
RIGHT: PE4, 左右：type 1 (EV_KEY), code 117 (KEY_KPEQUAL), value 1
X, PE11, 右上：type 1 (EV_KEY), code 120 (KEY_SCALE), value 1
B, PE12, 右下：type 1 (EV_KEY), code 119 (KEY_PAUSE), value 1
Y, PE2, 右左：type 1 (EV_KEY), code 118 (KEY_KPPLUSMINUS), value 1
A, PE13, 右右：type 1 (EV_KEY), code 121 (KEY_KPCOMMA), value 1
SELECT, PE8, 左1：type 1 (EV_KEY), code 122 (KEY_HANGUEL), value 1
START, PE9, 左2：type 1 (EV_KEY), code 123 (KEY_HANJA), value 1
MENU, PE3, 右1：type 1 (EV_KEY), code 124 (KEY_YEN), value 1
L, PE1，未焊接: Event code 125 (KEY_LEFTMETA)
R, PE10，未焊接: Event code 126 (KEY_RIGHTMETA)

https://bbs.aw-ol.com/topic/3751/全开源-小志掌機gaviar-handheld-资料汇总/9
https://bbs.aw-ol.com/topic/3650/gaviar-handheld-小志掌機/22?page=1
```

* work_getevent_v3.7z, work_getevent_v2.7z  
```
小志掌机研究。我尝试在树莓派4b上（方便编译运行）简化evtest代码，
得到大概只有120行左右的代码，如图，
核心部分是一个循环加select（经典select/poll模型），你可能好奇，
我如果要非阻塞或者同时读两个以上的设备输入怎么办？SDL和Android NDK
的做法是合并到同一个事件队列，写法很类似select/poll，
但可以做到非阻塞的轮询

小志掌机研究。关于按键输入方法，除了evtest的源码中select函数（通过循环+select+read读取gpio-key或者sysfs设备），
还可以通过poll函数，参考getevent的源码（见tina的一个包或者在gh找，源自Android源码），
以及mFlying/ssd2xx-demo和OpenNuvoton/N32926_Linux_Applications的GPIO示例。
ssd2xx-demo称之为中断方式读取输入
```
https://gitee.com/mFlying/ssd2xx-demo/blob/master/7.gpio/gpio_test_input/main.c  
http://doc.industio.com/docs/ido-som2d0x-start/ido-som2d0x-start-1ctpju1ek2b27  
https://github.com/OpenNuvoton/NUC970_Linux_Applications/blob/master/demos/gpio/gpio_demo.c  
https://github.com/OpenNuvoton/NUC980_Linux_Applications/blob/master/demos/gpio/gpio_demo.c  
https://github.com/OpenNuvoton/N32905_Linux_Applications/blob/master/gpio/gpio.c  
https://github.com/OpenNuvoton/N32926_Linux_Applications/blob/master/gpio/gpio.c  
https://github.com/markyzq/getevent_ubuntu  
https://github.com/freedesktop-unofficial-mirror/evtest  
evtest-1.34  
https://github.com/mangopi-sbc/tina-package/tree/main/utils/getevent  

* qt hide mouse and get keycode  
qt4-nes_v12_button_input_success.tar.gz  
```
小志掌机研究。研究按键输入问题（目前未解决），重新编译Qt4，发现几个以前搞错的地方：
（1）以前发现编译qt时ar报错，后来发现其实是因为我没有配置好正确的objcopy（指向错误的工具链），改好就没事了
（2）Qt4只能在ubuntu14（非32位版，64位版）下交叉编译，如果放在xubuntu20下会出现编译错误，
卡在QPrintDialog那里，那是因为Qt4无法用较新的host gcc编译（可能和uic生成ui_头文件的变量名有关）
（3）可以通过QWSServer::setCursorVisible(false)隐藏鼠标，用setOverrideCursor无效
（4）我试过用QWS_KEYBOARD=:/dev/input/event1指定键盘，虽然可以，
但发现获取的键码不对，我可能需要另外想办法

小志掌机研究。由于Qt4在小志掌机上的按键键码是乱的，我的想法是把evtest缩小版代码整个嵌入到用qt nes代码中，
通过Qt线程启动，如果用Windows编译大概就是如下效果——当然只能模拟编译，效果要需要试验。
我甚至看到有人用Qt网络库去读取linux input event设备事件，例如这篇
《Qt之 读取 /dev/input/event*设备 并解析》，不过这篇是触摸屏输入

小志掌机研究，我测试过通过嵌入evtest实现按键输入的思路是可行的，非常流畅地获得按键反馈，
可以开始选择左右移动跳跃和发射。相关的代码我会找机会上传到gh上，
也可能等最后一块功能音频输出研究好再做，我没有把握一定能解决Qt的音频输出，
如果实在搞不定就跳过，另外GamePi20的按键输入也需要研究，
那个相对会比较简单，因为WiringPi支持中断方式的按键输入函数ISR
```

## GamePi20, rpi zero    
* run rom  
2018-04-18-raspbian-stretch-lite.zip    

* qt4 nes  
https://github.com/nejidev/arm-NES-linux  

* fvjpeg6b_v4_xiaozhi.tar.gz  

* qt4 nes  
qt4-NES4_5_512_480_640_480_try_high_speed.7z   
qt4-nes_rp0.tar.gz  
qt4-nes2_v1_success_ubuntu14_qt4_qws.tar.gz  

* lvgl  
work_gamepi_v3.7z  
lv_port_linux_frame_buffer_gamepi20_v1.tar.gz

* https://github.com/darrenliew96/gamepi20_drivers

* https://github.com/rm-hull/st7735fb

* https://github.com/waveshare/mk_arcade_joystick_rpi

* https://github.com/waveshare/GamePi15  

## Waveshare ESP32-One + GamePi20, with Arduino IDE ESP32 plugin    
* ips2_0_esp32_2_esp32one_gamepi20_v1_wifi_no_auto_shutdown.7z
* ips2_0_esp32_esp32one_gamepi20_v5_wifi_no_auto_shutdown.7z
* https://www.waveshare.net/wiki/ESP32_One

## (TODO) Waveshare RP2040-PiZero  
* https://www.waveshare.net/wiki/RP2040-PiZero  

## 榴莲派 (compatible with LicheePi Nano) , f1c100s, 480x272    
* lvgl with buildroot  
lv_port_linux_frame_buffer_f1c_480_br_uclibc_v1.tar.gz  
lv_port_linux_frame_buffer_f1c_480_image_br_uclibc_v1.tar.gz  

* linux_4.15.0 with qt4  
flashimg_ubuntu140432_g++_ipc_nano_480_272_linux_4.15.0-rc8_uclibc.bin  
licheenano_480_ubuntu140432_v3_g++_ipc.tar.gz   
qt4nano_v3.tar.gz  
opt_qt_lib_fonts.zip  

* linux 5 with buildroot  
buildroot-tiny200-master_nano_v1.tar.gz  
sysimage-nor_480_272_aodzip_nano.img  

* burn nor flash  
mpi-r-tools.zip, zadig-2.5.exe, Device, Create New Device, Allwinner FEL Device, USB ID: 1F3A EFE8, Install Driver  
mpi-r-tools.zip, zadig-2.5.exe, Device, Create New Device, Allwinner DFU Device, USB ID: 1F3A 1010, Install Driver  
sunxi-fel.exe -p spiflash-write 0 xxx.bin  

## GAME BOX POWER M3, Sup M3, SupM3, F1C100s + 8MB nor flash    
* https://steward-fu.github.io/website/handheld.htm#q8
* https://github.com/steward-fu/archives/releases?q=q8&expanded=true
* https://github.com/steward-fu/archives/releases/download/q8/q8_od_jckl_no_roms.img.7z
* m3_factory_tf_4gb.7z  
* m3_2_factory_nor_flash.rar  
* m3_factory_tf_8gb.7z  
* m3_3.rar
* 焊接3 UART和2 FEL  
```
我又多了一个F1C100S开发板。如图，焊接Sup M3的三线串口和2线FEL开关，和运行Q8固件的串口日志。
其中2线FEL开关在HOME键旁边（外壳的正中间三个按键那里），短接后启动再松开进入FEL模式。
而3线串口在LCD下方nor flash的下面，方形焊台是GND，从右到左（图LCD反转到下方，
所以图中是从左到右）依次是GND，RX0，TX0（大概是这样，如果不对的话调转），
对应调试器的GND，TXD，RXD。我测试过出厂固件（运行在8mb nor flash）内是没有这个串口输出的，
但如果运行tf卡的Q8固件则有（这是第三方固件，要自己刷，出厂没有，但这个固件用不了，按键没匹配）
```
* lcd driver, cfw-2.0.0-alpha-14-gb39b67e.7z  
https://github.com/tiopex/sdcard/releases  
http://c.tieba.baidu.com/p/7691824426?pn=2  
console.cfg  
CONSOLE_VARIANT=bittboy2x  
BOOT_M3_mod.7z\variants\bittboy2x\modules.custom.sh  
insmod "../../r61520fb.ko" version=1 flip=1
* if use tf card with q8_od_jckl_no_roms.img.7z, it could be got a root login prompt in UART GRT pins
* q8_od_jutleys_no_roms.img.7z also works  
see https://github.com/steward-fu/archives/releases?q=q8&expanded=true  

## 小淘气开发板(xiaotaoqi), f1c200s, 800x480  
* licheenano_800_ubuntu140432_v4_g++_ipc.tar.gz  
flashimg_ubuntu140432_g++_ipc_nano_800_480_linux_4.15.0-rc8_uclibc.bin  

## LVGL Android  
* lvgldemo_v2_lvgl_android_draw_success.7z  
* VideoProject_v2_play_audio_success(1).7z  

## ubuntu visualbox framebuffer, directfb    
* test_v5_dfb177_ubuntu140432.tar.gz  
* dirkgroenen_fbv-master.zip  

## (TODO) WiringPi  
* WiringPi_WiringPi-master.zip  
* showbmp_luckfox_v1.tar.gz  

## (TODO) retro-go, retro-go-stm32, retro yao-mio  

## luckfox pico  
* soft spi, arm-rockchip830-linux-uclibcgnueabihf.tar.gz, Pico_LCD_Code.7z, VirtualBox-Luckfox-Pico-Ubuntu18.zip  
showbmp_luckfox_v5_1.44_bmp.zip  

## milk-v duo  
* soft spi, LF_Pico_LCD_Image.7z, milkv-duo-20230616-2232.img.zip, duo-sdk-v1.2.0.tar.gz, xubuntu200464  
showbmp_milkv_v2_img.tar.gz
showbmp_milkv_v1_basic.tar.gz


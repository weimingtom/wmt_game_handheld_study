# wmt_game_handheld_study
My game handheld study

## Gaviar-Handheld, 小志掌機, 小志掌机 (xiaozhi), Allwinner D1s    
* https://bbs.aw-ol.com/topic/3751/全开源-小志掌機gaviar-handheld-资料汇总/9  

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

## 小淘气开发板(xiaotaoqi), f1c200s, 800x480  
* licheenano_800_ubuntu140432_v4_g++_ipc.tar.gz  
flashimg_ubuntu140432_g++_ipc_nano_800_480_linux_4.15.0-rc8_uclibc.bin  

## LVGL Android  
* lvgldemo_v2_lvgl_android_draw_success.7z

* VideoProject_v2_play_audio_success(1).7z  

## ubuntu visualbox framebuffer, directfb    
* test_v5_dfb177_ubuntu140432.tar.gz

* dirkgroenen_fbv-master.zip


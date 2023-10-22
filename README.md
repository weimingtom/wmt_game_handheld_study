# wmt_game_handheld_study
My game handheld study

## 

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

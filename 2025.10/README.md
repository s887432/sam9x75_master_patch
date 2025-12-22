## The patch files for SAM9x75 MASTER board.<br>
https://www.microchip.com.tw/uploads/tad_uploader/tmp/590/APP_MASTERS25_2_Dev_Resource.pdf<br>
0000_sam9x75_master_buildroot_exteranl-2025.10.patch is the buildroot patch which combined all other patches.<br>
<br>
## How to build it
$ git clone https://github.com/linux4microchip/buildroot-mchp.git -b linux4microchip-2025.10<br>
$ git clone https://github.com/linux4microchip/buildroot-external-microchip.git -b linux4microchip-2025.10<br>
$ git clone https://github.com/s887432/sam9x75_master_patch<br>
$ cd buildroot-external-microchip<br>
$ git apply ../sam9x75_master_patch/2025.10/0000_sam9x75_master_buildroot_exteranl-2025.10.patch<br>
$ cd ../buildroot-mchp<br>
$ BR2_EXTERNAL=../buildroot-external-microchip make sam9x75_master_graphics_defconfig<br>
$ make -j16<br>
<br>
Have fun!!!<br>
Patrick

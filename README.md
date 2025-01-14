# zynq_dts_uboot
```plaintext
repositorio con dts de placas para uboot
para usar los dts
dejar el dts en la ruta: u-boot-xlnx/arch/arm/dts/$(board-name).dts
añadir al Makefile el nombre del dtb path u-boot-xlnx/arch/arm/dts/Makefile 
  en el grupo dtb-$(CONFIG_ARCH_ZYNQ) += \ -> $(board-name).dtb
añadir a u-boot-xlnx/configs/xilinx_zynq_virt_defconfig 
  en el label CONFIG_OF_LIST -> CONFIG_OF_LIST="..... $(board-name).dtb"
export CROSS_COMPILE=arm-linux-gnueabihf-
source /tools/Xilinx/Vivado/2022.2/settings64.sh
export DEVICE_TREE=$(board-name)
make xilinx_zynq_virt_defconfig
make -j $(nproc)
```

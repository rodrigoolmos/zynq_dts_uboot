# zynq_dts_uboot
repositorio con dts de placas para uboot
para usar los dts
dejar el dts en la ruta: u-boot-xlnx/arch/arm/dts/$(board-name).dts
añadir al Makefile el nombre del dts u-boot-xlnx/arch/arm/dts/Makefile -> $(board-name).dtb
export CROSS_COMPILE=arm-linux-gnueabihf-
source /tools/Xilinx/Vivado/2022.2/settings64.sh
export DEVICE_TREE=$(board-name)
make xilinx_zynq_virt_defconfig
make -j $(nproc)

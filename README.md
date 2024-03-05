# zynq_dts_uboot
repositorio con dts de placas para uboot
para usar los dts
dejar el dts en la ruta: u-boot-xlnx/arch/arm/dts/zynq-qmtech.dts
añadir al Makefile el nombre del dts u-boot-xlnx/arch/arm/dts/Makefile -> zynq-qmtech.dtb
export DEVICE_TREE=zynq-qmtech
make xilinx_zynq_virt_defconfig
make -j $(nproc)

################################################################################
HOW TO BUILD KERNEL FOR SPH-L600_SPR

1. How to Build
	- get Toolchain
	download and install arm-eabi-4.6 toolchain for ARM EABI.
	Extract kernel source and move into the top directory.

	$ make VARIANT_DEFCONFIG=msm8930_melius_spr_defconfig msm8930_melius_defconfig SELINUX_DEFCONFIG=selinux_defconfig
	$ make
	
2. Output files
	- Kernel : Kernel/arch/arm/boot/zImage
	- module : Kernel/drivers/*/*.ko
	
3. How to Clean	
    $ make clean
	
4. How to make .tar binary for downloading into target.
	- change current directory to Kernel/arch/arm/boot
	- type following command
	$ tar cvf SPH-L600_SPR.tar zImage
#################################################################################
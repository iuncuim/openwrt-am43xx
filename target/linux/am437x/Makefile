#
# Copyright (C) 2012-2014 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

ARCH:=arm
BOARD:=am437x
BOARDNAME:=TI AM437x
FEATURES:=usb usbgadget ext4 targz fpu audio display nand ubifs
CPU_TYPE:=cortex-a9
CPU_SUBTYPE:=vfpv3

KERNEL_PATCHVER:=4.9

MAINTAINER:=Alexander Couzens <lynxis@fe80.eu>

KERNELNAME:=zImage dtbs

define Target/Description
	TI AM437x boards
endef

include $(INCLUDE_DIR)/target.mk

$(eval $(call BuildTarget))

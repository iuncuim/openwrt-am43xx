#
# Copyright (C) 2012-2013 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk
include $(INCLUDE_DIR)/kernel.mk

PKG_VERSION:=2017.01
PKG_RELEASE:=2

PKG_HASH:=6c425175f93a4bcf2ec9faf5658ef279633dbd7856a293d95bd1ff516528ecf2

include $(INCLUDE_DIR)/u-boot.mk
include $(INCLUDE_DIR)/package.mk

define U-Boot/Default
  BUILD_TARGET:=am437x
  UBOOT_IMAGE:=u-boot.img MLO
  UENV:=default
endef

define U-Boot/am43xx_evm
  NAME:=AM43xx EVM
  BUILD_DEVICES:=am437x-sk-evm
endef

UBOOT_TARGETS:=am43xx_evm

define Build/InstallDev
	$(INSTALL_DIR) $(STAGING_DIR_IMAGE)/$(BUILD_DEVICES)
	$(CP) $(patsubst %,$(PKG_BUILD_DIR)/%,$(UBOOT_IMAGE)) $(STAGING_DIR_IMAGE)/$(BUILD_DEVICES)/
	$(CP) ./files/uEnv-$(UENV).txt $(STAGING_DIR_IMAGE)/$(BUILD_DEVICES)/uEnv.txt
endef

$(eval $(call BuildPackage/U-Boot))

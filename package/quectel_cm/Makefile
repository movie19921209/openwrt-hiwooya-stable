#
# Copyright (C) 2008-2010 OpenWrt.org
# Copyright (C) 2016 fly.zhu <flyzjhz@gmail.com>
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=quectel_cm
PKG_VERSION:=1.0.0
PKG_RELEASE:=1

PKG_MAINTAINER:=fly.zhu <flyzjhz@gmail.com>
PKG_LICENSE:=GPL-2.0

include $(INCLUDE_DIR)/package.mk

define Package/quectel_cm
  SECTION:=base
  CATEGORY:=Base system
  DEPENDS:= +libpthread
  TITLE:=quectel_cm communication utility
endef


define Build/Prepare
	mkdir -p $(PKG_BUILD_DIR)
	$(CP) ./src/* $(PKG_BUILD_DIR)/
endef

# define Build/Compile
# 	CFLAGS="$(TARGET_CPPFLAGS) $(TARGET_CFLAGS)" \
# 	$(MAKE) -C $(PKG_BUILD_DIR) \
# 		$(TARGET_CONFIGURE_OPTS) \
# 		LIBS="$(TARGET_LDFLAGS) -lm -lpthread"
# endef

define Package/quectel_cm/install
	$(INSTALL_DIR) $(1)/usr/sbin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/quectel-CM $(1)/usr/sbin/fournet

endef

$(eval $(call BuildPackage,quectel_cm))

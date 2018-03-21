#
# Copyright (C) 2014 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=luciipk
PKG_VERSION:=2015-08-17
PKG_RELEASE=$(PKG_SOURCE_VERSION)


PKG_MAINTAINER:=tieniu <blogic@openwrt.org>
PKG_LICENSE:=GPL-2.0+

include $(INCLUDE_DIR)/package.mk

define Package/luciipk
  SECTION:=utils
  CATEGORY:=Utilities
  TITLE:=OpenWrt LUCI ipk
  DEPENDS:=+uhttpd +uhttpd-mod-ubus \
        +luci-app-firewall +luci-proto-ppp +libiwinfo-lua +lua +libuci-lua +rpcd +libubus-lua
endef

define Build/Prepare
endef

define Build/Configure
endef

define Build/Compile
endef

define Package/luciipk/install
	$(INSTALL_DIR) $(1)/etc/init.d 
	$(INSTALL_DIR) $(1)/root
	$(INSTALL_BIN) ./files/luciipk.luci $(1)/etc/init.d/luciipk
	$(INSTALL_BIN) ./files/*.ipk $(1)/root/
endef

$(eval $(call BuildPackage,luciipk))

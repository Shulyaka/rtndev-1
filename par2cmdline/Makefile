#
# Copyright (C) 2011-2016 Entware
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=par2cmdline
PKG_VERSION:=0.6.14-20160630
PKG_REV:=b0fab491b2055320ab2996a48c00f417911c79f0
PKG_RELEASE:=1

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.bz2
PKG_SOURCE_SUBDIR:=$(PKG_NAME)-$(PKG_VERSION)
PKG_SOURCE_URL:=https://github.com/Parchive/par2cmdline.git
PKG_SOURCE_PROTO:=git
PKG_SOURCE_VERSION:=$(PKG_REV)

PKG_FIXUP:=autoreconf
PKG_INSTALL:=1

include $(INCLUDE_DIR)/package.mk

define Package/par2cmdline
	SECTION:=utils
	CATEGORY:=Utilities
	DEPENDS:=+libstdcpp
	TITLE:=file verification and repair tool
	URL:=$(PKG_SOURCE_URL)
	MAINTAINER:=Entware team, http://entware.net
endef

define Package/par2cmdline/description
 par2cmdline is a PAR 2.0 compatible file verification and repair tool.
endef

define Package/par2cmdline/install
	$(INSTALL_DIR) $(1)/opt/bin
	$(INSTALL_BIN) $(PKG_INSTALL_DIR)/opt/bin/par2 $(1)/opt/bin
	$(FIND) $(PKG_INSTALL_DIR)/opt/bin -type l -exec $(CP) -a {} $(1)/opt/bin \;
endef

$(eval $(call BuildPackage,par2cmdline))

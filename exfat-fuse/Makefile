#
# Copyright (C) 2011-2016 Entware
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=exfat-fuse
PKG_VERSION:=1.2.4
PKG_REV:=82764a7a8cdfa778efbffd59fdc7a15726ff50f4
PKG_RELEASE:=1

PKG_FIXUP:=autoreconf
PKG_INSTALL:=1

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.bz2
PKG_SOURCE_SUBDIR:=$(PKG_NAME)-$(PKG_VERSION)
PKG_SOURCE_URL:=https://github.com/relan/exfat.git
PKG_SOURCE_PROTO:=git
PKG_SOURCE_VERSION:=$(PKG_REV)

include $(INCLUDE_DIR)/package.mk

define Package/exfat-fuse
	SECTION:=utils
	CATEGORY:=Utilities
	SUBMENU:=Filesystem
	DEPENDS:=+fuse-utils +libpthread
	TITLE:=a full-featured exFAT file system implementation
	URL:=https://github.com/relan/exfat
	MAINTAINER:=Entware team, http://entware.net
endef

define Package/exfat-fuse/description
 This project aims to provide a full-featured exFAT file system implementation for Unix-like systems.
 It consists of a FUSE module (fuse-exfat) and a set of utilities (exfat-utils).
endef



define Package/exfat-fuse/install
	$(INSTALL_DIR) $(1)/opt/sbin
	$(CP) $(PKG_INSTALL_DIR)/opt/sbin/* $(1)/opt/sbin
endef

$(eval $(call BuildPackage,exfat-fuse))

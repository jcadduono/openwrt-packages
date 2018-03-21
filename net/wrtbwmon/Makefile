include $(TOPDIR)/rules.mk

PKG_NAME:=wrtbwmon
PKG_VERSION:=0.36
PKG_RELEASE:=1
PKG_LICENSE:=GPL-2.0

PKG_MAINTAINER:=

include $(INCLUDE_DIR)/package.mk

define Package/wrtbwmon
  SECTION:=net
  CATEGORY:=Network
  TITLE:=LEDE Per-User Bandwidth Monitoring
endef

define Package/wrtbwmon/description
wrtbwmon is a small and basic shell script designed to provide per user
bandwidth monitoring capabilities and generate usage reports.
endef

define Build/Compile
endef

define Package/wrtbwmon/install
	$(INSTALL_DIR) $(1)/usr/sbin
	$(INSTALL_BIN) ./files/wrtbwmon $(1)/usr/sbin/wrtbwmon
	$(INSTALL_BIN) ./files/readDB.awk $(1)/usr/sbin/readDB.awk
	$(INSTALL_DIR) $(1)/usr/share/wrtbwmon
	$(INSTALL_DATA) ./files/usage.htm1 $(1)/usr/share/wrtbwmon/usage.htm1
	$(INSTALL_DATA) ./files/usage.htm2 $(1)/usr/share/wrtbwmon/usage.htm2
	$(INSTALL_DIR) $(1)/etc/init.d
	$(INSTALL_BIN) ./files/wrtbwmon.init $(1)/etc/init.d/wrtbwmon
endef

$(eval $(call BuildPackage,wrtbwmon))

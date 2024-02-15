include $(TOPDIR)/rules.mk

PKG_NAME:=luci-app-autotimeset
PKG_VERSION:=2.0.2
PKG_RELEASE:=20230718

LUCI_TITLE:=LuCI support for Scheduled Time setting by ssw 2024.02.15
LUCI_PKGARCH:=all
LUCI_DEPENDS:=+luci-compat

define Package/$(PKG_NAME)/conffiles
/etc/config/autotimeset
endef

include $(TOPDIR)/feeds/luci/luci.mk

# call BuildPackage - OpenWrt buildroot signature

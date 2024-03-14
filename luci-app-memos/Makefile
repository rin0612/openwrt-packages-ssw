

include $(TOPDIR)/rules.mk

PKG_VERSION:=1.0.2-20231208
PKG_RELEASE:=

LUCI_TITLE:=by ssw 2024.03.14
LUCI_PKGARCH:=all
LUCI_DEPENDS:=+lsblk +docker +luci-lib-taskd

define Package/luci-app-memos/conffiles
/etc/config/memos
endef

include $(TOPDIR)/feeds/luci/luci.mk

# call BuildPackage - OpenWrt buildroot signature

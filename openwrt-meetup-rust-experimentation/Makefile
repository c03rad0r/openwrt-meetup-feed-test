include $(TOPDIR)/rules.mk

PKG_NAME:=openwrt-meetup-rust-experimentation
PKG_VERSION:=1.0.0
PKG_RELEASE:=1

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/c03rad0r/openwrt-meetup-rust-experimentation.git
PKG_SOURCE_VERSION:=master

PKG_BUILD_DEPENDS:=rust/host

include $(INCLUDE_DIR)/package.mk
include ../../packages/lang/rust/rust-package.mk

define Package/openwrt-meetup-rust-experimentation
  SECTION:=net
  # Select package by default
  #DEFAULT:=y
  CATEGORY:=Network
  TITLE:=OpenWrt Rust Experimentation
  DEPENDS:=$(RUST_ARCH_DEPENDS)
  URL:=https://www.github.com/c03rad0r/openwrt-meetup-rust-experimentation
  SUBMENU:=VPN
endef

define Package/openwrt-meetup-rust-experimentation/description
  An experimental Rust package for OpenWrt.
endef

# define Cargo/Configure
#   --no-default-features
# endef


# define Build/Prepare
#   mkdir -p $(PKG_BUILD_DIR)
#   $(CP) ./src/* $(PKG_BUILD_DIR)/
# endef

# define Build/Configure
# # Nothing to do here for us.
# # By default openwrt-meetup-rust-experimentation/src/Makefile will be used.
# endef

# define Build/openwrt-meetup-rust-experimentation/Compile
#   CFLAGS="$(TARGET_CFLAGS)" CPPFLAGS="$(TARGET_CPPFLAGS)" $(MAKE) -C $(PKG_BUILD_DIR) $(TARGET_CONFIGURE_OPTS)
# endef

# define Package/openwrt-meetup-rust-experimentation/install
#   $(INSTALL_DIR) $(1)/usr/sbin
#   $(INSTALL_BIN) $(PKG_BUILD_DIR)/openwrt-meetup-rust-experimentation $(1)/usr/sbin/
# endef

$(eval $(call RustBinPackage,openwrt-meetup-rust-experimentation))
$(eval $(call BuildPackage,openwrt-meetup-rust-experimentation))

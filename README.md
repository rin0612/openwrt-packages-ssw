自用备份插件库 by ssw
```
rm -rf package/openwrt-packages/luci-app-ddnsto
rm -rf package/openwrt-packages/ddnsto

git clone https://github.com/rin0612/openwrt-packages-ssw  package/openwrt-packages-ssw
 
make package/openwrt-packages-ssw/${包名,例如homebox}/compile V=s
```

```
<*> luci-app-ddnsto
    <> ddnsto
        https://github.com/linkease/nas-packages/tree/master/network/services/ddnsto
            by 2024.02.09
    <> luci-app-ddnsto
        https://github.com/linkease/nas-packages-luci/tree/main/luci/luci-app-ddnsto
            by 2024.02.09

<*> luci-app-homebox
    <> homebox
        https://github.com/sirpdboy/netspeedtest/tree/master/homebox
            by 2024.02.09
    <> luci-app-homebox
        https://github.com/jjm2473/openwrt-apps/tree/main/luci-app-homebox
            by 2021.12.29 checkout 0be31f3c183abb205ff897ff15d1a3e9ce132446
        https://github.com/jjm2473/openwrt-apps/tree/main/homebox
            此仓库此版本homebox已无法编译(提示make[4]: go-bindata: Command not found)
                解决方案(未验证)
                    go get -modcacherw github.com/go-bindata/go-bindata/...; \
                    go install -modcacherw github.com/go-bindata/go-bindata/...@latest; \
                    $(GO_PKG_VARS) PATH=$$$$PATH:$(PKG_BUILD_DIR)/.go_work/build/bin \
                    $(GO_PKG_VARS) PATH=$(PKG_BUILD_DIR)/.go_work/build/bin:$$$$PATH \

<*> luci-app-gowebdav
    <> gowebdav
        https://github.com/immortalwrt-collections/openwrt-gowebdav/trunk/gowebdav
            by 2022.04.25
    <> luci-app-gowebdav
        https://github.com/immortalwrt-collections/openwrt-gowebdav/trunk/luci-app-gowebdav
            by 2022.04.25

<*> luci-app-autotimeset
    <> luci-app-autotimeset
        https://github.com/sirpdboy/luci-app-autotimeset
            by 2022.04.25

<*> luci-app-poweroff
    <> luci-app-poweroff
        https://github.com/esirplayground/luci-app-poweroff
            by 2022.04.25
```

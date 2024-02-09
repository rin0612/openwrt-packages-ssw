# openwrt-packages-ssw
自用备份插件库

```
LuCI ---> Applications --->
<*> luci-app-ddnsto
    <>ddnsto
        https://github.com/linkease/nas-packages/tree/master/network/services/ddnsto
            by 2024.02.09
    <>luci-app-ddnsto
        https://github.com/linkease/nas-packages-luci/tree/main/luci/luci-app-ddnsto
            by 2024.02.09

<*> luci-app-homebox
    <>homebox
        https://github.com/sirpdboy/netspeedtest/tree/master/homebox
            by 2024.02.09
    <>luci-app-homebox
        https://github.com/jjm2473/openwrt-apps/tree/main/luci-app-homebox
            by 2021.12.29 checkout 0be31f3c183abb205ff897ff15d1a3e9ce132446
        https://github.com/jjm2473/openwrt-apps/tree/main/homebox
            此仓库此版本homebox已无法编译(提示make[4]: go-bindata: Command not found)
                解决方案(未验证)
                    go get -modcacherw github.com/go-bindata/go-bindata/...; \
                    go install -modcacherw github.com/go-bindata/go-bindata/...@latest; \
                    $(GO_PKG_VARS) PATH=$$$$PATH:$(PKG_BUILD_DIR)/.go_work/build/bin \
                    $(GO_PKG_VARS) PATH=$(PKG_BUILD_DIR)/.go_work/build/bin:$$$$PATH \
```

自用备份插件库 by ssw

暂时不用的备份在本仓库backup分支

注意, 使用本仓库执行make menuconfig, 只有app-title显示by ssw才是本仓库的
例如：< > luci-app-argonne-config... LuCI page for Argonne Config by ssw 2022.04.25
```
git clone https://github.com/rin0612/lede -b backup.2022.04.25 openwrt
cd openwrt
./scripts/feeds update -a
./scripts/feeds install -a
git clone https://github.com/rin0612/openwrt-packages-ssw  package/openwrt-packages-ssw
git clone https://github.com/rin0612/openwrt-packages package/openwrt-packages -b backup.2022.04.25
git clone https://github.com/rin0612/small package/small -b backup.2022.04.25

rm -rf package/openwrt-packages/UnblockNeteaseMusic
rm -rf package/openwrt-packages/luci-app-unblockneteasemusic
rm -rf package/openwrt-packages/luci-theme-argon
rm -rf package/openwrt-packages/luci-app-argon-config
rm -rf package/openwrt-packages/luci-theme-argonne
rm -rf package/openwrt-packages/luci-app-argonne-config
rm -rf package/openwrt-packages/ddnsto
rm -rf package/openwrt-packages/luci-app-ddnsto
rm -rf package/small/luci-app-openclash

rm -rf feeds/packages/net/zerotier
rm -rf feeds/packages/net/baidupcs-web
rm -rf feeds/packages/multimedia/UnblockNeteaseMusic
rm -rf feeds/packages/multimedia/UnblockNeteaseMusic-Go
rm -rf feeds/luci/applications/luci-app-zerotier
rm -rf feeds/luci/applications/luci-app-unblockmusic
rm -rf feeds/luci/applications/luci-app-baidupcs-web
```

```
<*> luci-app-ddnsto
    <> ddnsto
        https://github.com/linkease/nas-packages/tree/master/network/services/ddnsto
            by ssw 2024.02.09
    <> luci-app-ddnsto
        https://github.com/linkease/nas-packages-luci/tree/main/luci/luci-app-ddnsto
            by ssw 2024.02.09

<*> luci-app-homebox
    <> homebox
        https://github.com/jjm2473/openwrt-apps/tree/main/homebox
            by ssw 2024.02.22
            备注: 
                homebox[by ssw 2024.02.22]和luci-app-homebox[by ssw 2021.12.29]正常使用
                此仓库历史版本homebox无法编译(提示make[4]: go-bindata: Command not found),解决方案(未验证): 
                    go get -modcacherw github.com/go-bindata/go-bindata/...; \
                    go install -modcacherw github.com/go-bindata/go-bindata/...@latest; \
                    $(GO_PKG_VARS) PATH=$$$$PATH:$(PKG_BUILD_DIR)/.go_work/build/bin \
                    $(GO_PKG_VARS) PATH=$(PKG_BUILD_DIR)/.go_work/build/bin:$$$$PATH \
    <> homebox 
        https://github.com/sirpdboy/netspeedtest/tree/master/homebox
            此仓库此版本homebox[by 2024.02.09]无法和luci-app-homebox[by ssw 2021.12.29]使用,luci菜单不出来(对比两个版本Makefiel估计是files文件夹和etc中的配置缺少)
    <> luci-app-homebox
        https://github.com/jjm2473/openwrt-apps/tree/main/luci-app-homebox
            by ssw 2021.12.29 checkout 0be31f3c183abb205ff897ff15d1a3e9ce132446

<*> luci-app-gowebdav
    <> gowebdav
        https://github.com/immortalwrt-collections/openwrt-gowebdav/trunk/gowebdav
            by ssw 2022.04.25
    <> luci-app-gowebdav
        https://github.com/immortalwrt-collections/openwrt-gowebdav/trunk/luci-app-gowebdav
            by ssw 2022.04.25

<*> luci-app-autotimeset
    <> luci-app-autotimeset
        https://github.com/sirpdboy/luci-app-autotimeset
            by ssw 2024.02.15

<*> luci-app-poweroff
    <> luci-app-poweroff
        https://github.com/esirplayground/luci-app-poweroff
            by ssw 2022.04.25

<*> luci-theme-argonne
    <> luci-theme-argonne
        https://github.com/kenzok8/openwrt-packages/tree/master/luci-theme-argonne
            by ssw 2022.04.25
    <> luci-app-argonne-config
        https://github.com/kenzok8/openwrt-packages/tree/master/luci-theme-argonne-config
            by ssw 2022.04.25
    备注：
        openwrt argon主题 https://github.com/jerrykuku/luci-theme-argon/blob/master/README_ZH.md
        原先编译的主题是这个： https://github.com/kenzok78/luci-theme-argonne
        这个主题就是argon，目前这个仓库又重定向了： https://github.com/kenzok78/luci-theme-argone

<*> luci-app-zerotier
    <> zerotier
        https://github.com/coolsnowwolf/packages/tree/master/net/zerotier
            by ssw 2024.02.15
    <> luci-app-zerotier
         https://github.com/coolsnowwolf/luci/tree/master/applications/luci-app-zerotier
            by ssw 2024.02.15

<*> luci-app-unblockmusic
    <> UnblockNeteaseMusic
        https://github.com/coolsnowwolf/luci/tree/master/applications/luci-app-unblockmusic
            by ssw 2024.02.16
    <> UnblockNeteaseMusic-Go
        https://github.com/coolsnowwolf/packages/tree/master/multimedia/UnblockNeteaseMusic-Go
            by ssw 2024.02.16
    <> luci-app-unblockmusic
        https://github.com/coolsnowwolf/packages/tree/master/multimedia/UnblockNeteaseMusic
            by ssw 2024.02.16

<*> luci-app-baidupcs-web
    <> luci-app-baidupcs-web
        https://github.com/coolsnowwolf/luci/tree/master/applications/luci-app-baidupcs-web
            by ssw 2024.02.16
    <> baidupcs-web
        https://github.com/coolsnowwolf/packages/tree/master/net/baidupcs-web
            by ssw 2024.02.16

<*> luci-app-openclash
    < > luci-app-openclash
        https://github.com/vernesong/OpenClash
            by ssw 2024.03.03
```

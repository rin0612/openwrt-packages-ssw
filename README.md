自用备份插件库 by ssw

这些是暂时不用的备份
```
<> baidupcs-go      TODO待处理(疑似已弃用)
    https://github.com/coolsnowwolf/packages/tree/master/net/baidupcs-go
        by ssw 2024.02.16

<*> luci-app-zerotier TODO待处理(这两个一起使用存在问题，首次无法启动，启动了重启后才能启动，启动了无法关闭，user.notice luci-zerotier: Service status isn't running!)
    <> zerotier
        https://github.com/coolsnowwolf/packages/tree/master/net/zerotier
            by ssw 2024.02.15
    <> luci-app-zerotier
        https://github.com/zhengmz/luci-app-zerotier
            by ssw 2024.02.15

<*> luci-app-homebox TODO待处理(homebox和luci-app-homebox这两个版本在一起luci菜单不显示)
    <> homebox
        https://github.com/sirpdboy/netspeedtest/tree/master/homebox
            by ssw 2024.02.09
    <> luci-app-homebox
        https://github.com/jjm2473/openwrt-apps/tree/main/luci-app-homebox
            by ssw 2021.12.29 checkout 0be31f3c183abb205ff897ff15d1a3e9ce132446
     
<> luci-app-openclash      TODO待处理(未测试)
    https://github.com/rin0612/openwrt-packages/luci-app-openclash
        by ssw 2024.03.03
```

netspeedtest
```
增加feed源
echo >> feeds.conf.default
echo 'src-git sirpdboy_netspeedtest https://github.com/sirpdboy/netspeedtest' >> feeds.conf.default
./scripts/feeds update sirpdboy_netspeedtest
./scripts/feeds install -a -p sirpdboy_netspeedtest
集成软件包
make menuconfig
选择软件包
LuCI ---> Applications --->
<*> luci-app-netspeedtest...................... LuCI Support for netspeedtest
备注：选择luci-app-netspeedtest后会带上iperf3和python3相关的多个包作为依赖
```

ddnsto
```
增加feed源
echo >> feeds.conf.default
echo 'src-git linkease_nas https://github.com/linkease/nas-packages.git;master' >> feeds.conf.default
echo 'src-git linkease_nas_luci https://github.com/linkease/nas-packages-luci.git;main' >> feeds.conf.default
./scripts/feeds update linkease_nas linkease_nas_luci
./scripts/feeds install -a -p linkease_nas
./scripts/feeds install -a -p linkease_nas_luci
集成软件包
make menuconfig
选择软件包
LuCI ---> Applications --->
<*> luci-app-ddnsto.................................. LuCI support for ddnsto
备注：无法编译，如果只编译ddnsto可以luci-app-ddnsto和ddnsto文件夹拷贝出来
```

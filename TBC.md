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

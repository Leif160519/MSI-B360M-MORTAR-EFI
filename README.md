# MSI-B360M-MORTAR-EFI

## EFI-AMD
配置：
- CPU：I5-9600K
- 主板：微星B360M迫击炮
- 内存：16GB DDR4 8GBX2
- 硬盘：西数黑盘NVME+Intel 760P 250GB
- 显卡：AMD Vega 56蓝宝石
- OS： 10.14

## EFI-NVIDIA
配置：
- CPU: I5-9600K
- 主板：微星B360M迫击炮
- 内存：32GB DDR4 16GBX2
- 硬盘：Sansumg 850 PRO 128GB
- 显卡：ASUS GTX 1080
- OS：10.13.6

## 注意
若`-v` 启动时提示版本不兼容之类的信息，请在`config.plist`中的`boot`选项中添加`-no_compat_check`参数跳过系统版本检查，这种情况一般在smbios较新，而安装的系统版本较旧的时候出现，即所安装的系统版本低于smbios机型出厂的系统版本(如:smbios选择macmini 8,1但是系统版本却安装10.13.6)
```
	<key>Boot</key>
	<dict>
		<key>Arguments</key>
		<string>-v -no_compat_check</string>
        ....
```

# Dell 7560 OpenCore EFI


- BigSur 11.4 亲测正常

## 在线安装方法

```shell

# Lion(10.7):
python macrecovery.py -b Mac-2E6FAB96566FE58C -m 00000000000F25Y00 download
python macrecovery.py -b Mac-C3EC7CD22292981F -m 00000000000F0HM00 download

# Mountain Lion(10.8):
python macrecovery.py -b Mac-7DF2A3B5E5D671ED -m 00000000000F65100 download

# Mavericks(10.9):
python macrecovery.py -b Mac-F60DEB81FF30ACF6 -m 00000000000FNN100 download

# Yosemite(10.10):
python macrecovery.py -b Mac-E43C1C25D4880AD6 -m 00000000000GDVW00 download

# El Capitan(10.11):
python macrecovery.py -b Mac-FFE5EF870D7BA81A -m 00000000000GQRX00 download

# Sierra(10.12):
python macrecovery.py -b Mac-77F17D7DA9285301 -m 00000000000J0DX00 download

# High Sierra(10.13)
python macrecovery.py -b Mac-7BA5B2D9E42DDD94 -m 00000000000J80300 download
python macrecovery.py -b Mac-BE088AF8C5EB4FA2 -m 00000000000J80300 download

# Mojave(10.14)
python macrecovery.py -b Mac-7BA5B2DFE22DDD8C -m 00000000000KXPG00 download

# Catalina(10.15)
python macrecovery.py -b Mac-00BE6ED71E35EB86 -m 00000000000000000 download

# Latest version
# ie. Big Sur(11)
python macrecovery.py -b Mac-E43C1C25D4880AD6 -m 00000000000000000 download

```

- 将下载的两个文件（`BaseSystem.dmg`、`BaseSystem.chunklist`）放入 `com.apple.recovery.boot` 目录下

- 目录结构如下

```text
├── EFI
│	├── BOOT
│	└── OC
└── com.apple.recovery.boot
 	├── BaseSystem.chunklist
 	└── BaseSystem.dmg
```

- 准备一个1G以上的优盘，然后格式化

- 将目录结构下的文件拷贝个优盘的根目录

> 注意，上面的目录结构最好不要保留其他文件，可能会有其他状况发生

- 重启电脑，在启动选项里选择优盘中的`OpenCore.efi`启动即可

## 耳机🎧解决

进入 `ComboJack` 目录，执行 `ComboJack_Installer/install.sh` 文件即可。


## 其他说明
- 安装macOS Big Sur的过程很漫长 , 请耐心等待 , 不一定是有错误
- 每次升级或替换新的EFI后 , 最好重置一下NVRAM

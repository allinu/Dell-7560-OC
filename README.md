# Dell 7560 OpenCore EFI


- BigSur 11.4 亲测正常

## 在线安装方法

```shell
Lion
./macrecovery.py -b Mac-2E6FAB96566FE58C -m 00000000000F25Y00
./macrecovery.py -b Mac-C3EC7CD22292981F -m 00000000000F0HM00

Mountain Lion:
./macrecovery.py -b Mac-7DF2A3B5E5D671ED -m 00000000000F65100

Mavericks
./macrecovery.py -b Mac-F60DEB81FF30ACF6 -m 00000000000FNN100

Yosemite:
./macrecovery.py -b Mac-E43C1C25D4880AD6 -m 00000000000GDVW00

El Capitan
./macrecovery.py -b Mac-FFE5EF870D7BA81A -m 00000000000GQRX00

Sierra
./macrecovery.py -b Mac-77F17D7DA9285301 -m 00000000000J0DX00

High Sierra
./macrecovery.py -b Mac-7BA5B2D9E42DDD94 -m 00000000000J80300
./macrecovery.py -b Mac-BE088AF8C5EB4FA2 -m 00000000000J80300

Mojave
./macrecovery.py -b Mac-7BA5B2DFE22DDD8C -m 00000000000KXPG00

Catalina
./macrecovery.py -b Mac-CFF7D910A743CAAF -m 00000000000PHCD00
./macrecovery.py -b Mac-00BE6ED71E35EB86 -m 00000000000000000

Diagnostics
./macrecovery.py -b Mac-E43C1C25D4880AD6 -m 00000000000000000 -diag
./macrecovery.py -b Mac-E43C1C25D4880AD6 -m 00000000000GDVQ00 -diag
./macrecovery.py -b Mac-E43C1C25D4880AD6 <real MLB> -diag

Default version
./macrecovery.py -b Mac-E43C1C25D4880AD6 -m 00000000000GDVQ00       (oldest)
./macrecovery.py -b Mac-E43C1C25D4880AD6 -m <real MLB> -os default  (newer)

Latest version
./macrecovery.py -b Mac-E43C1C25D4880AD6 -m 00000000000000000 -os latest
./macrecovery.py -b Mac-E43C1C25D4880AD6 -m <real MLB> -os latest

```

- 将下载的两个文件（`BaseSystem.dmg`、`BaseSystem.chunklist`）放入 `com.apple.recovery.boot` 目录下

- 目录结构如下

```text
├── EFI
│	├── Dell
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

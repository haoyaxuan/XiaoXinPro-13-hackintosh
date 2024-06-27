# XiaoXinPro-13 2020
## 电脑配置

| 规格   | 详细信息                              |
|------|-----------------------------------|
| 电脑型号 | XiaoXinPro13 2020                 |
| 处理器  | Intel i7-10710U（六核）               |
| 内存   | 海力士 DDR4 16GB                     |
| 硬盘   | UMIS 512GB M.2 Nvme               |
| 集成显卡 | Intel HD Graphics CFL CRB         |
| 独立显卡 | GeForce MX350 2G（Disable）         |
| 声卡   | Realtek ALC257                    |
| 网卡   | Intel AX201（Replace BCM94360CS2 ） |


## 正常功能：
- [x] CPU变频
- [x] 显卡（独显在BIOS中直接禁用）
- [x] 睡眠，Win下无法深度睡眠，Mac下可以
- [x] 触摸板，支持完美手势
- [x] 网卡，Intel AX201 WIFI正常驱动，蓝牙无法使用空投和接力，其他完美，想要全完美建议更换`白果拆机卡`。
- [x] 硬盘，不要用三星和海力士的，建议使用西数SN720
- [x] HiDPI，建议使用[RDM](https://github.com/haoyaxuan/XiaoXinPro-13-hackintosh/raw/main/hackintool/RDM.zip)


## 镜像下载
-  [MacOS Monterey 12.5](https://osx.cx/macos-monterey-12-5-21f79.html)
- 感谢 @黑果小兵 @黑苹果社区


## BIOS设置
* 需要刷测试版BIOS，[BIOS Beta CLCN32WW.DPC10.rar](https://github.com/haoyaxuan/XiaoXinPro-13-hackintosh/raw/main/hackintool/BIOS%20Beta%20CLCN32WW.DPC10.rar)
* Fn+F2进入BIOS
* Security -> Secure Boot：勾选Disable
* Advanced -> System Agent -> Graphics Configura -> DVMT PreAllocated：勾选64M
* Advanced -> Power Performanc -> CPU Power Manage -> CPU Lock Configura -> CFG Lock：勾选Disable


## 不刷BIOS 设置CFG lock和DVMT
* 将[EFI-shell](https://github.com/haoyaxuan/XiaoXinPro-13-hackintosh/raw/main/hackintool/EFI-shell.zip)解压后复制到U盘，改名为EFI，然后从U盘启动，进入EFI Shell界面
* 设置 Pre-Allocated DVMT 为 64M:
  ***setup_var 0x107 0x02***
* 禁用 CFG lock:
  ***setup_var 0x3E 0x00***


## 注意
- 睡眠，请使用[睡眠脚本](https://github.com/haoyaxuan/XiaoXinPro-13-hackintosh/raw/main/hackintool/睡眠脚本.zip)解压后，执行`双击设置睡眠模式25.command`。
- 部分i5的 CPUID 为 `0x0A0660`，需要仿冒cpuid ：`0x0806EC`、`0x0806EB` 或其他），详情看[这里](https://github.com/daliansky/XiaoXinPro-13-hackintosh/wiki/%E6%9F%A5%E7%9C%8B%E6%9C%AC%E6%9C%BACPUID)
- 其他详细教程可以查看[黑果小兵 小新Pro13 EFI](https://github.com/daliansky/XiaoXinPro-13-hackintosh)，再次感谢 @黑果小兵


## 更新日志
- 2024.06.12 Upgrade OC 0.9.3
- 2023.01.04 升级OC0.8.7，解决睡眠问题。
- 2022.09.22 全新EFI，fork [黑果小兵 小新Pro13 EFI](https://github.com/daliansky/XiaoXinPro-13-hackintosh)

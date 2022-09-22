# DELL-7472
## 电脑配置

| 规格   | 详细信息                              |
|------|-----------------------------------|
| 电脑型号 | XiaoXinPro13 2020                 |
| 处理器  | Intel i5-10210U                   |
| 内存   | 海力士 DDR4 16GB                     |
| 硬盘   | UMIS 512GB M.2 Nvme               |
| 集成显卡 | Intel HD Graphics CFL CRB                      |
| 独立显卡 | GeForce MX350 2G（Disable）         |
| 声卡   | Realtek ALC257                    |
| 网卡   | Intel AX201（Replace BCM94360CS2 ） |


## 正常功能：
1：显卡 （核显正常，独显禁用）


## 镜像下载
-  [MacOS Monterey 12.5](https://osx.cx/macos-monterey-12-5-21f79.html)
- 感谢 @黑果小兵 @黑苹果社区

## BIOS设置
* Secure Boot -> Secure Boot Enable：勾选Disable

## BIOS设置 For 隐项
* 将EFI-shell文件夹复制到U盘，改名为EFI，然后从U盘启动
* 设置 Pre-Allocated DVMT 为 64M:
  ***setup_var 0x107 0x02***
* 禁用 CFG lock:
  ***setup_var 0x3e 0x00***


## 更新日志
- 2021.04.20 全新EFI

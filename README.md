# handover-list
工作交接列表

## Notebook Model
* AM8/AM8A-Monet 
* AM9C-Pandora3
    * Ubuntu & Windows 10 双系统，Download 完 test image 后默认从 Ubuntu 系统启动自动执行脚本跑 AMD Diag 测试 PASS 后自动切换到 Windows 10 进行 FFT 测试。
    * 安装双系统及配置 Ubuntu 测试 Diag 环境请参考。。。
    * Ubuntu 自动执行脚本配置
        * 编辑 sudo nano /etc/default/grub 文件修改 GRUB_TIMEOUT=10 -> GRUB_TIMEOUT=10, 然后执行 sudo update-grub
        * 更改 Ubuntu Boot Entry 默认启动顺序，编辑/boot/grub/grub.cfg,修改 set default="${saved_entry}" 为 set default="0"
        * 添加开机自动执行脚本，sudo nano ~/.bashrc, 在.bashrc文件最后一行新增需要开机启动自动执行的 bash 指令 （例：sudo bash /home/diag/..../AMD_Diag_Go.sh）
        * How to avoid the "S to skip" message on ubuntu boot?如何避免Ubuntu系统启动时停在某个地方按某个键跳过，add the option nobootwait to your /etc/fstab  /boot/grub/grub.cfg

* Notebook 机种 shop-floor 维护地址 \\\172.26.6.116 (User:qms Password:qms)

* Utility(WIN BASE SF 系统-维护半机 Engine 线 BIOS)  \\\172.26.6.116\nb1_winbase_sf\Shopfloor\Utility\Loader\Loader.exe (User:07061031 Password:07061031)

* WIN_Utility(WIN 整机 shop-floor 系统)   \\\172.26.6.116\nb1_wincto_sf\AppExe\WIN_UT\LOADER\Loader.exe (User:07061031 Password:07061031)
    * Pilot run BIOS: SWDL Maintain - Pilot Run BIOS - Upload pilot run BIOS excel 文档

## Non-Notebook Model
Mainmenu(SMT 治具电脑绑定) \\\172.26.21.116\smt_nb1_exe\MainMenu\Mainmenu

CS_UTw(查询 IoT 机种测试 log )   \\\172.26.6.116\nb1_wincto_sf\AppExe\CS_UT\Loader\Loader.exe (User:07061031 Password:07061031)

Loader(绑定站别治具电脑)   \\\172.26.6.116\nb1_wincto_sf\AppExe\DefineTest\LOADER\Loader.exe (User:A2052373 Password:A2052373)

### IoT 试产新机种 (NPI)
* QF6
* ABOB-Savant
* KUD-Dyson
* 0WM-Facebook

### IoT 量产机种 (MP)
* H6A-SmartHost

關於 Smart host 會有三種不同的 model number(Smart host, S2 及 S12) 一事, 客人決定採用同一個 image 且不用於出貨時重刷 shipping image 的方式, 而以燒入於機器中的 Part number 來做區分.
客人採用這個方法應對工廠的投產這三個產品, 也是好事, 同一個 PCBA, 同個產測方法, 只要於寫入part number時要寫對 part number.

針對如何知道要寫入那個part number, 我的想法如下, 要請大家看這個想法是否可行:

1.	這三個產品, 其貼於底部的label, 所以, 其packaging BOM上的內容物不同且所放置的QSG也不同, 所以, 應可依此建立新的1字階料號
2.	客人的訂單會提供要出那個model number
3.	依客人訂單上所列的model number, 開工單時, 可以知道其對應到的廣達1字階料號, 且此時廣達的S/N應也已設定好
4.	Shop floor系統上存有1字階料號所對應到的要燒入到機器的 part number
5.	在進行燒入 part number 時, 作業員掃瞄待測機的廣達S/N, 從廣達S/N可以知道其1字階料號, 再由1字階料號可取得要燒錄的part number, 取得後做燒錄的動作.


* H6C-SmartAudio(Host PC 端软体安装,驱动安装 H6C 与 H6A 均一致)
    * ZOC debug 工具，安装路径 \\\172.26.6.72\nb1tool\常用工具\H6A安装工具\zoc651.exe
    * 治具单片机 COM Port 驱动，安装路径 \\\172.26.6.72\nb1tool\常用工具\H6A安装工具\DriverCOMxian
    * 产品 COM Port 驱动，安装路径 \\\172.26.6.72\nb1tool\常用工具\H6A安装工具\DriverCOMxian

* Remote (Host PC 测试软件部署)
    * ZOC debug 工具，安装路径 \\\172.26.6.72\nb1tool\常用工具\H6A安装工具\zoc651.exe
	* SLT1/SLT3/SLT3-1, 治具单片机 COMPort 驱动，安装路径 \\\172.26.6.72\nb1tool\常用工具\H6A安装工具\DriverCOMxian
    * SLT2 MIC 测试软体驱动，安装路径 \\\172.26.6.72\nb1tool\常用工具\H6A-RM安装工具\Engine_SDTMIC\LVRTE2013std.exe
    * SLT2/SLT4 产品ADB驱动，安装路径 \\\172.26.6.72\nb1tool\常用工具\H6A-RM安装工具\android_device_usb_driver
    * SLT5 安捷伦U2001A驱动，安装路径 \\\172.26.6.72\nb1tool\常用工具\安捷伦U2001A安装\IOLibSuite_16_3_17914.exe

* Remote-base

* QF7

* UU1 - 智能自行车锁
    SLT1/SLT2 两站测试类似，SLT1 是半机测试， SLT2 是整机测试

* H60 - 
    * RD 的执行脚本以及 UART command, log 等列表 \\\172.26.6.72\nb1tool\常用工具\H60测试交接\Test_item_table-20151125.xlsx
    * 利用 wifi 更新 DUT 端 image 的功能；\\\172.26.6.72\nb1tool\常用工具\H60测试交接\H60_PVT_download_image_tool.pptx
    * DUT 端 4 个 tool 及其参数使用：1. factory_test 2. factory_tool.sh 3. qci_test 4. fw_update.sh \\\172.26.6.72\nb1tool\常用工具\H60测试交接\H60_uart_command_screenshot.zip
    * 正常 image下，factory_test 和 factory_tool.sh 都存在，如果只有其中一个，则说明 image 已经在 recovery image 下了。解决方法是参考 H60_PVT_download_image_tool.pptx 刷 image
    * Host PC 需要安装的 Tool 和 driver，已经放于服务器上： \\\172.26.6.72\nb1tool\常用工具\勿删-H60_Tools_Drivers

* H60_PM2.5

### POS-Panasonic



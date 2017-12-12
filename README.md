# handover-list
工作交接列表

## Notebook 
* AM8 - EOL
* AM9C
    * BIOS 窗口 W.Z Peng 彭武晟
    * 测试 Image 为 UEFI mode，没有纯 Dos 环境，AMD Diag 是在 Linux 环境下 run。双系统环境 Ubuntu + Windows，PQC download 测试 image 后先切到 Ubuntu 环境下 run diag，diag pass 后自动切换到 Windows 下进行 function 测试。
* Notebook 机种 shop-floor 维护地址 \\172.26.6.116 (User:qms Password:qms)

* Utility(WIN BASE SF 系统-维护半机 Engine 线 BIOS)  \\172.26.6.116\nb1_winbase_sf\Shopfloor\Utility\Loader\Loader.exe (User:07061031 Password:07061031)

* WIN_Utility(WIN 整机 shop-floor 系统)   \\172.26.6.116\nb1_wincto_sf\AppExe\WIN_UT\LOADER\Loader.exe (User:07061031 Password:07061031)
    * Pilot run BIOS: SWDL Maintain - Pilot Run BIOS - Upload pilot run BIOS excel 文档

## Non-Notebook
Mainmenu(SMT 治具电脑绑定) \\172.26.21.116\smt_nb1_exe\MainMenu\Mainmenu

CS_UTw(查询 IoT 机种测试 log )   \\172.26.6.116\nb1_wincto_sf\AppExe\CS_UT\Loader\Loader.exe (User:07061031 Password:07061031)

Loader(绑定站别治具电脑)   \\172.26.6.116\nb1_wincto_sf\AppExe\DefineTest\LOADER\Loader.exe (User:A2052373 Password:A2052373)

### IoT 试产新机种 (NPI)
* QF6
    * SMT 两站,崇基预烧 factory image， BLT1 大板功能测试，BT/WIFI SMT 扫 RSSI即可，BLT2小板测试
    * FA 两站， RunIn(offline) - FRT - FFT - Recovery(offline)
* ABOB-Savant
    * ABOB-MCI
        * MCI Audio 测试中的 tool A85*.exe 不 support 32 位系统，所以 Host PC 必须用 64 位系统
        * Com port 1 为 Uart，Com port 2，3 分别是 RS232，Com port 4 为 MCU 单片机
        * SMT/FA 需要用到治具测试部分 两颗LED（SMT 只测试亮灭，FA 还测试灯号颜色，LED1 绿色，LED2 绿色+红色），IR1-6, 
        * ABOB 治具指令请参考***
        * Audio 测试需安装 Python 环境
    * ABOB-MCO
        * Com port 1 为 Uart，Com port 4 为 MCU 单片机
        * SMT/FA 需要用到治具测试部分 两颗LED（SMT 只测试亮灭，FA 还测试等号颜色），GPIO, Audio 
* KUD-Dyson
* 0WM-Facebook

### IoT 量产机种 (MP)
* H6A SmartHost 系列不完全指北 (SHC-2000, SHC-S2, SHC-S12, SMS-1001, SMS-100AM)
    * SMT BLT0 目前已整合 SHC,SMS 和 S2 的 image 烧录，根据 MB serial number 来区分烧录 ubootmfg。
    * BLT0(Uboot烧录站)
H6A-SHC-S2 50料头的MB，Uboot烧录已经跟H6A 30/40料头整合到一起，程式会根据MBSN自动区分烧录30/40/50料头的Uboot，请copy "\\172.26.21.210\nb1tool\TestProgram\H6A\BLT0_30_40_50共用版" 文件夹下的BLT0烧录使用。


* BLT1(功能测试站）
    * 注意BLT1精简版30/40/50料头的可以共用一版测试程式，全测的因为每个料头测试的item不一样所以不能共用一版请区分使用。

* H6C-SmartAudio(Host PC 端软体安装,驱动安装H6C与H6A均一致)
    * ZOC debug 工具，安装路径 \\172.26.6.72\nb1tool\常用工具\H6A安装工具\ zoc651.exe
    * 治具单片机 COM Port 驱动，安装路径 \\172.26.6.72\nb1tool\常用工具\H6A安装工具\DriverCOMxian
    * 产品 COM Port 驱动，安装路径 \\172.26.6.72\nb1tool\常用工具\H6A安装工具\DriverCOMxian

* Remote (Host PC 测试软件部署)
    * ZOC debug 工具，安装路径 \\\172.26.6.72\nb1tool\常用工具\H6A安装工具\zoc651.exe
	* SLT1/SLT3/SLT3-1, 治具单片机 COMPort 驱动，安装路径 \\\172.26.6.72\nb1tool\常用工具\H6A安装工具\DriverCOMxian
    * SLT2 MIC 测试软体驱动，安装路径 \\\172.26.6.72\nb1tool\常用工具\H6A-RM安装工具\Engine_SDTMIC\LVRTE2013std.exe
    * SLT2/SLT4 产品ADB驱动，安装路径 \\\172.26.6.72\nb1tool\常用工具\H6A-RM安装工具\android_device_usb_driver
    * SLT5 安捷伦U2001A驱动，安装路径 \\\172.26.6.72\nb1tool\常用工具\安捷伦U2001A安装\IOLibSuite_16_3_17914.exe

* QF7
* UU1 - 智能自行车锁
    SLT1/SLT2 两站测试类似，SLT1 是半机测试， SLT2 是整机测试·

* H60 - 
    * RD 的执行脚本以及 UART command, log 等列表 \\172.26.6.72\nb1tool\常用工具\H60测试交接\Test_item_table-20151125.xlsx
    * 利用 wifi 更新 DUT 端 image 的功能；\\172.26.6.72\nb1tool\常用工具\H60测试交接\H60_PVT_download_image_tool.pptx
    * DUT 端 4 个 tool 及其参数使用：1. factory_test 2. factory_tool.sh 3. qci_test 4. fw_update.sh \\172.26.6.72\nb1tool\常用工具\H60测试交接\H60_uart_command_screenshot.zip
    * 正常 image下，factory_test 和 factory_tool.sh 都存在，如果只有其中一个，则说明 image 已经在 recovery image 下了。解决方法是参考 H60_PVT_download_image_tool.pptx 刷 image
    * Host PC 需要安装的 Tool 和 driver，已经放于服务器上： \\172.26.6.72\nb1tool\常用工具\勿删-H60_Tools_Drivers

* H60_PM2.5

### POS 机

* \\172.26.6.25\capt\POS_HSW\DL3_WIM
* 


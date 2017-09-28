# handover-list
工作交接列表

## Notebook 
* AM8 - 
* AM9C

## Non-Notebook

### IoT 试产新机种 (NPI)
* QF6
* ABOB-Savant
* KUD-Dyson
* 0WM-Facebook

### IoT 量产机种 (MP)
* H6A-SmartHost
* H6C-SmartAudio
* Remote (Host PC 测试软件部署)
    * ZOC debug 工具，安装路径 \\\172.26.6.72\nb1tool\常用工具\H6A安装工具\zoc651.exe
	* SLT1/SLT3/SLT3-1, 治具单片机 COMPort 驱动，安装路径 \\\172.26.6.72\nb1tool\常用工具\H6A安装工具\DriverCOMxian
    * SLT2 MIC 测试软体驱动，安装路径 \\\172.26.6.72\nb1tool\常用工具\H6A-RM安装工具\Engine_SDTMIC\LVRTE2013std.exe
    * SLT2/SLT4 产品ADB驱动，安装路径 \\\172.26.6.72\nb1tool\常用工具\H6A-RM安装工具\android_device_usb_driver
    * SLT5 安捷伦U2001A驱动，安装路径 \\\172.26.6.72\nb1tool\常用工具\安捷伦U2001A安装\IOLibSuite_16_3_17914.exe
* Remote-base
* QF7
* UU1 - 智能自行车锁
* H60 - 
    * RD 的执行脚本以及 UART command, log 等列表 \\172.26.6.72\nb1tool\常用工具\H60测试交接\Test_item_table-20151125.xlsx
    * 利用 wifi 更新 DUT 端 image 的功能；\\172.26.6.72\nb1tool\常用工具\H60测试交接\H60_PVT_download_image_tool.pptx
    * DUT 端 4 个 tool 及其参数使用：1. factory_test 2. factory_tool.sh 3. qci_test 4. fw_update.sh \\172.26.6.72\nb1tool\常用工具\H60测试交接\H60_uart_command_screenshot.zip
    * 正常 image下，factory_test 和 factory_tool.sh 都存在，如果只有其中一个，则说明 image 已经在 recovery image 下了。解决方法是参考 H60_PVT_download_image_tool.pptx 刷 image
    * Host PC 需要安装的 Tool 和 driver，已经放于服务器上： \\172.26.6.72\nb1tool\常用工具\勿删-H60_Tools_Drivers

* H60_PM2.5

### POS 机



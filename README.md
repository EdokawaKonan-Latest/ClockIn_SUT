# ClockIn_SUT

**打开此脚本时请勿开启vpn, 开启vpn会使服务器找不到你真实ip而使打卡失败**  
一个仅适用与SUT学生的自动疫情打卡脚本, 暂不支持mac os(主要我没用过不知道把文件放哪XD)   
该脚本会自动抓取你前一天的打卡记录, 并根据前一天的打卡信息完成今天的打卡(也就是说如果你换了地方后的第一天就得自己打卡了)  
第一次启动该脚本后需要输入账号和密码, 之后启动不需要, 完成打卡后脚本会自动退出
## Windows环境开机自动开启此脚本
如果你有python环境, 使用pip安装requests包, 将python脚本放在一个特定位置, 然后创建一个bat批处理文件, 内容如下(假定python存放位置为D:\\Temp):
```bat
python D:\Temp\main.py
```
如果你没有python环境, 下载release中的ClockIn.exe, 然后创建一个bat文件, 内容如下(假定exe文件存放位置为D:\\Temp):
```bat
D:\Temp\ClockIn.exe
```
然后将bat文件移动到Windows启动目录(C:\Users\你的Windows账户名\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Startup), 就可在每次系统启动时唤起程序, 完成自动打卡

### 2021.02.03 更新
添加提示"昨日未打卡的错误提示"

### 2021.02.16 更新
添加对意外异常的捕获, 现在脚本在遇到一些异常情况时不会直接退出而是打印异常

### 2021.04.30 更新
添加网络链接失败后重试选项

### 2021.10.04 更新
修复无法打卡问题
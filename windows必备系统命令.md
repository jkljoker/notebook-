# Windows必备系统命令

## windows快捷键命令

win + D 进入电脑桌面

win + E  打开文件管理器

win + L 锁屏	

win + TAB 打开项目预览页

win + v 打开剪切板历史

Alt + TAB 切换项目



Ctrl + S 保存

Ctrl + A 全选

Ctrl + c 复制

Ctrl + v 粘贴

Ctrl + x 剪切

Ctrl + z 撤销 



win + R + cmd 打开cmd窗口

win + R + mspaint 打开微软画板

win + R + notepad 打开记事本

win + R + regedit 打开注册表管理

win + R + services.msc 打开服务管理

win + R + mstsc 打开远程管理

win + R + msconfig 打开启动项管理



## Windos基本内部命令=

### md

功能：创建目录

格式：

mkdir [drive:]path

md [drive:]path

例子：

md \test 在该盘符的根目录创建一个test文件夹

md test1 在当前目录创建test1目录

md 1\2\3\4 在当前目录创建一个1\2\3\4的递归目录

md C:\test 在C盘根目录创建一个test1文件夹

### rd

功能：删除一个目录

格式：

rmdir [/s][/q][drive:]path

rd [/s][/q][drive:]path

例子：

rd test 删除test目录

rd 1 /s 删除1递归目录

rd 1 /s/q 删除1递归目录，不要求确定

### cd

功能：显示当前目录名或改变当前目录

格式：

chdir [/d][drive:][path]

chdir [..]

cd [/d][drive:][path]

cd [..]

例子：

cd 显示当前所在路径或改变当前所在目录

cd test1 进入test1目录

cd /d c:\ 切换到c盘根目录

cd /d d:\ 切换到d盘根目录

cd /d c:\test 进入c盘根目录下的test目录（当前在D盘）

cd . >a.txt 创建一个a.txt文件

### dir 显示磁盘目录命令

功能：显示磁盘目录的内容

格式：

dir [盘符] [路径] [文件名] [/p] [/w] [/A[[:]属性]] [/O[:]排列顺序] [/s]

例子：

dir \Windows /p  分页显示Windows目录下的目录信息，按任意键继续查看

dir /w 只显示当前目录下的文件名

dir /a:d 显示该目录下的目录文件

dir /a:r 显示该目录下的只读文件

dir /a:h 显示该目录下的隐藏文件

dir /o:n 按字母顺序排列

dir /o:s 按大小（从小到大）排列

dir /o:d 按日期/时间（从先到后）排列

dir test /s 显示test目录和所有子目录中的文件

### copy

功能：将一份或多份文件复制到另一个位置

格式：

COPY [/D] [/V] [/N] [/Y] [/-Y] [/Z] [/L] [/A] [/B] source [/A | /B] [+ source[/A | /B] [+ ...]] [destination [/A | /B]]

例子：

copy nul a.txt 创建一个a.txt文件

copy test1 test2 将test1中的文件全部复制到test2目录中

copy test1 test2 /y 不提示确定 将test1中的文件全部复制到test2目录中

copy a.txt + b.txt + c.txt + d.txt e.txt 将a,b,c.txt的内容整合到d.txt中

### echo

功能：显示信息，或将命令回显打开或关上

格式：

echo [message]

例子：

echo 123 直接输出123

echo a > a.txt 把字母a和回车换行**覆盖**输出到a.txt

echo b >> a.txt 把字母b和回车换行**追加**输出到a.txt

### type

功能：显示文件内容命令

格式：

type [盘符：] [路径] <文件名>

例子：

type a.txt 查看a.txt中的内容（类似于Linux中的cat）

more a.txt 分页查看a.txt中内容（类似于Linux中的more）

### ren

功能：更改文件名称

格式：

ren [盘符:] [路径] <旧文件名><新文件名>

### del

功能：删除指定文件

格式：

del [盘符：] [ 路径] <文件名> [/p]

例子：

del 1.txt 直接删除1.txt

del 1.txt /p 删除前询问是否删除

del *.txt 删除当前目录下文件后缀名为.txt的所有文件

### date

功能：设置或显示系统日期

格式：date [yy-mm-dd]

例子：date 显示日期

date 2020/03/28

date 2020-04-28

### ren

功能:更改文件名称

例子：

ren 1.txt 2.txt 将1.txt重命名成2.txt

### time

功能：设置或显示系统日期

例子：

time 查看当前时间

time 15:30:00 修改时间为15：30分

w32tm /resync 同步时间

### cls

功能：清楚屏幕上的所有显示，光标置于屏幕左上角

用法：cls



## Windows文件系统命令

### assoc

功能：显示或修改文件拓展名关联

用法：

assoc 显示所有当前文件拓展名关联的列表

assoc .xml 显示xml关联的文件

assoc .xml= 删除xml关联

assoc .xml=xmlfile 给文件添加关联

![image-20231124173326367](../assets/image-20231124173326367.png)

### attrib

功能：显示、设置或删除文件或目录的只读、存档、系统以及隐藏属性

例子：

attrib 查看当前目录下所有文件的属性

attrib /d 查看当前目录下所有文件属性

attrib /s 查看当前目录下所有文件包括递归目录下所有文件的属性

attrib a.txt 查看指定文件a.txt的属性

attrib +r +h +s +a +i a.txt 给a.txt赋予只读，隐藏，系统，存档以及索引5个属性

attrib -h -s a.txt 给a.txt除去隐藏，系统两个属性

### move

功能：将一个或多个文件从一个目录移动到指定的目录

用法：

move 1.txt test1 将1.txt剪切到test1目录

move test1 test2 将test1目录重命名成test2目录（如果该目录下没有test2目录）

move test1 test2 将test1目录移动到test2目录

move 1.py 2.py 将1.py重命名成2.py

### tree

功能：以图形的方式显示路径或驱动器中磁盘的目录结构

用法：

tree 以图形的方式显示文件

tree /a 使用ASCII字符，而不使用拓展字符

tree /f 显示每个文件夹中文件的名称



## Windows网络相关的命令

### ping

功能：Ping是用于检测网络连通性、可到达性和域名解析的TCP/IP命令

例子:

ping -n 3 baidu.com 连续发送3个数据包给baidu.com

ping -t baidu.com 持续地ping baidu.com 直到人为中断（Ctrl + C可以中断ping命令）

ping -l 123 baidu.com 以每个数据字节数为123发送给baidu.com服务器

（字节数范围0-65500）

### ipconfig

功能：获得主机的配置信息，包括IP地址，子网掩码和默认网关

例子：

ipconfig /all 显示所有网络适配器（网卡、拨号连接等）的完整TCP/IP配置信息

ipconfig /displaydns 显示本机上的DNS域名解析列表

ipconfig /flushdns 清楚DNS缓存

ipconfig /release 释放IP

ipconfig /renew 重新获取IP

### tracert

功能：进行网络诊断，并且列出分组经过的路由节点，以及它在IP网络中每一条的延迟

例子：

tracert baidu.com 通过baidu.com 域名来追踪到达服务器的节点信息

tracerrt 36.152.44.96 通过IP地址来追踪到达服务器的节点信息

### Arp

功能：显示和修改IP地址与MAC地址之间的映射关系

例子：

arp -a 将显示出所有arp信息

arp -d 清楚arp缓存信息

### netUser

功能：添加或更改用户账号或显示用户账户信息

例子：

net user 用户名 密码 /add 建立用户

net user 用户名 /del 删除用户

net user 查看账户

net user 账户名 查看指定账户信息

query user 查看当前在线的用户

### Net start/Stop service

功能：启动/停止服务指令

例子：

net start 查看本机已启动的服务

net stop Everything 停止everything

net start Everything 开启everything

### netsh

功能：Netsh 是命令行脚本实用工具，它允许从贝蒂或远程显示或修改当前正在运行的计算机网络配置

例子：

netsh /? 查看netsh用法

netsh wlan show profiles 查看WIFI热点

netsh wlan show profiles name ="WIFI名称" key =clear 查看指定Wifi的配置信息

### netstat

功能：显示协议同济信息和当前TCP/IP连接

例子：

net start 查看本机运行的所有服务

netstat -ano 查看本机所有的TCP，UDP端口连接及其对应的pid

netstat -anob 查看本机所有的TCP，UDP端口连接，pid及其对应的发起程序

netstat -ano | findstr "ESTABLISHED"查看当前正处于连接状态的端口及其IP

netstat -ano | findstr "LISTENING"查看当前正处于监听状态的端口及其IP

netstat -ano | findstr"TIME_WAIT"

## Windows系统管理命令

### shutdown

功能：关机

例子：

shutdown -s 这个会弹出自动关机对话框，默认30秒后关机

shutdown -s -t 3600 1小时后自动关机

at 20:00 shutdown -s 添加1一条关机任务

### tsaklist

功能：用来查看进程

例子：

tasklist 查看本机进程

tasklist | findstr PID 根据进程的PID号来查询指定进程

### taskkill

功能：用来关闭进程

例子：

taskkill /pid 11500

taskkill /IM notepad.exe
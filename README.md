# 此项目基于flippy的67+o和67+打包N1的openwrt

# 快照功能
![Alt text](https://github.com/hublj/N1dabao-1/blob/main/img/R.jpeg)

使用方法：固件新刷入或采用新版的 update-xxx-openwrt.sh 脚本升级之后就具备了快照功能，工具包名称：由于取名困难，故采用了 flippy 为命令名称（/usr/sbin/flippy)，在ssh或ttyd下输入即可，全程中文菜单，全交互式操作。

# 默认IP及密码
默认IP 192.168.1.201  密码 password

# N1全新安装
 下载对应版本固件
 
 将固件写入U盘或TF卡 推荐写盘软件 rufu或者balenaEtcher任选其一
 
 插入U盘启动盒子，输入192.168.1.201进入后台
 
 在系统——TTYD终端——输入用户名root；密码password
 
 输入安装命令 cd root ./install-to-emmc.sh
 
 如果显示挂载失败，重新执行上述安装命令./install-to-emmc.sh

# N1在线升级方法
 
 cd /mnt/mmcblk2p4
 
 wget 升级脚本为openwrt-update-amlogic
 
 wget .gz后缀名的固件链接,鼠标右击后缀.gz文件获取链接地址
 
 gzip -d 上一步下载的固件全名
 
 chmod + x openwrt-update-amlogic
 
 ./openwrt-update-amlogic 之后有提示，输入y为保留配置升级，选n相当于重装。升级完成后系统会自动重启，稍安勿躁


# 自动更新说明
 固件采用自动编译，Acrions将会在每天监控上游代码是否更新，如passwall ssrp等，一旦检测到上游代码更加将会自动编译打包，于每天上午7时30分发布最新版固件。

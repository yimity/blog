注意事项：
Linux在内核4.9的版本加入了该bbr算法，所以必须要升级你的内核版本到4.9才能使用bbr。

安装步骤：
执行 以下命令
wget --no-check-certificate https://raw.githubusercontent.com/yimity/blog/master/bbr.sh && bash bbr.sh
(若出现 wget: command not found 错误，请自行按照自己的发行版安装 wget，一般都有)

按任意键继续安装，会列出来目前可用的内核版本列表，选择一项。

安装完成，提示是否重启系统，输入y，并回车，重启系统，如果不重启的话bbr是不会生效的。

检查结果
执行以下命令
lsmod | grep bbr
如果有提示 tcp_bbr 则安装成功。


# bbr.sh
 - 来自于https://github.com/teddysun/across/

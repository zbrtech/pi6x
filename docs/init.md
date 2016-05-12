烧录系统
配置树莓派

修改键盘布局
树莓派默认是英式键盘设置(你若❤️英，便是米旗)，不然要改成美式通用键盘

#sudo dpkg-reconfigure keyboard-configuration
选择 Generic 101-key PC -> Other -> English (US) -> English(US, alternative international)
#sudo reboot 
现在你可以放肆的使用你的键盘了

修改时区
只在树莓派上找到了上海的时区
输入命令 sudo dpkg-reconfigure tzdata
选择 Asia -> Shanghai
输出 Current default time zone: 'Asia/Shanghai'



修改软件源
由于系统默认的源在国外，大部分国内（墙外用户自便）用户更新软件的时候，速度比较慢
vi /etc/apt/source.list
deb http://mirrors.tuna.tsinghua.edu.cn/raspbian/raspbian/ wheezy main contrib non-free rpi 
deb-src http://mirrors.tuna.tsinghua.edu.cn/raspbian/raspbian/ wheezy main contrib non-free rpi 
deb http://mirrors.neusoft.edu.cn/raspbian/raspbian/ wheezy main contrib non-free rpi 
deb-src http://mirrors.neusoft.edu.cn/raspbian/raspbian/ wheezy main contrib non-free rpi 
deb http://mirrors.ustc.edu.cn/raspbian/raspbian/ wheezy main contrib non-free rpi 
deb-src http://mirrors.ustc.edu.cn/raspbian/raspbian/ wheezy main contrib non-free rpi
#Dalian Neusoft University of Information
deb http://mirrors.neusoft.edu.cn/raspbian/raspbian/ wheezy main contrib non-free rpi
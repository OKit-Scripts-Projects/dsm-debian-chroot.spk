## 换163源

0. vim /etc/apt/sources.list

0. 删除原来内容的或者用#注释掉

0. 添加
```
deb http://mirrors.163.com/debian/ jessie main non-free contrib
deb http://mirrors.163.com/debian/ jessie-updates main non-free contrib
deb http://mirrors.163.com/debian/ jessie-backports main non-free contrib
deb-src http://mirrors.163.com/debian/ jessie main non-free contrib
deb-src http://mirrors.163.com/debian/ jessie-updates main non-free contrib
deb-src http://mirrors.163.com/debian/ jessie-backports main non-free contrib
deb http://mirrors.163.com/debian-security/ jessie/updates main non-free contrib
deb-src http://mirrors.163.com/debian-security/ jessie/updates main non-free contrib
```


## 添加中文支持
0. `apt update # 完成上面的换源操作以后再执行这个步骤，不然一般来讲是很慢的` 
0. `apt upgrade`
0. `dpkg-reconfigure tzdata # asia / shanghai`
0. `apt install locales`
0. `dpkg-reconfigure locales`
0. 第一个界面：选择 en_US.UTF-8, zh_CN.GB2312, zh_CN.GB18030, zh_CN.GBK, zh_CN.UTF-8 
0. 第二个界面：Default 选 en_US.UTF-8

## 其他优化
0. `apt-get install software-properties-common`

## fish
```
echo 'deb http://download.opensuse.org/repositories/shells:/fish:/release:/2/Debian_8.0/ /' > /etc/apt/sources.list.d/shells:fish:release:2.list
apt-get update
apt-get install fish
```
```
wget -nv https://download.opensuse.org/repositories/shells:fish:release:2/Debian_8.0/Release.key -O Release.key
apt-key add - < Release.key
apt-get update
```

## 安装桌面

## 安装远程桌面

## 安装浏览器桌面

## 安装 calibre

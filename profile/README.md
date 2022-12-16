# exTHmUI 10 Treble

## 废话
这个项目承载着我梦想的第一步，那是在2020年9月的时候，刚入学初一，手机还是小米5，我在宽上看到了这个项目，开始尝试自己编译。当时什么都不会，走一步看一步，在21年换iPhone之后逐渐也搁置了，21年年底，有了荣耀10，又开始研究PHH Treble，之前exTHmUI 11就是我一个月的成果。22年1月也算正式迈入Android开发的行列，维护小米6X的Miku UI到现在。

昨天用荣耀10的时候，鸿蒙实在太卡了，原来用ex-11的体验也不是很好，所以从昨天中午开始给ex-10合ASB，构建GSI，这个项目主要为华为做支持，当然也支持别的设备，至于bug，反馈，能力范围内能修就修。现在时间也不大够，截止写这些废话时，距离中考大概还有190天吧。

## 构建GSI
系统要求：Ubuntu 18.04+

配置要求：16G内存 200G可用空间 4c Cpu

如果你想要无障碍构建，那么依赖的安装肯定你必须要会，这里不做叙述

你可以选择手动和半自动编译

### 手动
先在你的Home目录建一个工作目录
```
mkdir exthm-10-treble
cd exthm-10-treble
```
从本组织的android仓库init repo
```
repo init -u https://github.com/exthmui-10-treble/android --depth=1
```
然后
```
lunch exthm_treble_arm64_bvN
make systemimage
```

### 半自动
先在你的Home目录建一个工作目录
```
mkdir exthm-10-treble
cd exthm-10-treble
```
clone本组织的script
```
git clone https://github.com/exthmui-10-treble/script
```
运行脚本
```
bash script/build.sh
```

等待构建结束，在~/builds目录拿包

## 感谢
- [exTHmUI](https://github.com/exthmui-legacy)
- Miku UI

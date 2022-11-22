# hi3798mv100-openwrt
https://bbs.histb.com/d/226-ec6108v9-openwrt
免责申明：本镜像为Jimmy自用，一切资料来源网上，仅供尝鲜好玩。

下载地址：https://gitee.com/chanjinn/hi3798mv100-openwrt

尝鲜须知：
1、测试过的平台是EC6018V9，整包使用HiTool下载参考雕神的ubuntu镜像方式；
2、将在HiTool中kernel分区选择hi_kernel-4.4.y-EC6018V9-openwrt.bin
3、需要在HiTool的ubuntu分区选择rootfs-a7-openwrt-1G-usbnet.ext4

rootfs-a7-openwrt-1G-usbnet.ext4
a、rootfs里设置的/etc/config/network中默认把eth0当成lan口，必须使用usb外扩的eth1来接入入
b、eth0的内网lan网段是 192.168.89.1 ； eth1为wan使用dhcp来获取外网；
c、wifi 使用softap模式，账号 hi3798mv100，密码 Hi3798mv100

已知问题：
1、mv100自带eth0为百兆，测试过屏蔽eth0过两个usb用千兆usb网口（rtl8153和ax88179）下载速度依然只有12.5MB/s，上传速度可达30MB/s，本固件依然是自带eth0，usb为eth1。
2、usb驱动支持rtl8153和ax88179，其他的没测。
3、usb网卡概率出现从1Gbps编程1Mbps，原因未知，重启就好了，没兴趣研究。
![image](https://user-images.githubusercontent.com/23007737/203189748-10e1754d-3744-47fd-9dc7-d6c36ba97e46.png)
![image](https://user-images.githubusercontent.com/23007737/203189858-8d0c7618-ca92-44a6-87ff-5dbe64fda508.png)


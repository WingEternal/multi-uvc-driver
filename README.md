# Multi-Uvc-Driver
* A modified uvc driver for launching multiple uvc cameras, inspired by this [article](https://blog.csdn.net/zhangwu1241/article/details/52983271)
* Built and tested on ubuntu 20.04 LTS with kernel v5.13.0. The origin source code is fork from [here](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git
) and checkout to v5.13 (commit 62fb9874f5da54fdb243003b386128037319b219)
* The maximum payload transfer size is set to 0x800 (2048).
## Usage
* If you are working on the same kernel, download [release](https://github.com/WingEternal/multi-uvc-driver/releases/tag/v0.1)
* Otherwise try to build from source (I can't guarantee that it will work, but just try it)
```bash
git clone https://github.com/WingEternal/multi-uvc-driver.git
make
```
* Then unload the original driver and install the new one
```bash
sudo rmmod uvcvideo
sudo insmod ./uvcvideo.ko
```
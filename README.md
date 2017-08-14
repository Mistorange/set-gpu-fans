# set-gpu-fans
Controlling the fan speed of an NVIDIA GPU on a headless linux system requires spoofing a display.
This can be used to gain a few percent additonal performance, at the cost of increased noise.
For installation and usage, read the comments in cool_gpu.

# 服务器无桌面动态调节GPU风扇速度

```
git clone https://github.com/liqiang311/set-gpu-fans.git
cp -r $PWD/set-gpu-fans /opt
apt-get update
apt-get install -y xinit
service lightdm stop
cd /opt/set-gpu-fans
chmod +x cool_gpu
chmod +x nvscmd
./cool_gpu > controller.log 2>&1 &
```

参考:

http://www.jianshu.com/p/ab956df5e40c

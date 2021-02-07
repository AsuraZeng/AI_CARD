# os 
ubuntu 18.04.1 LTS

# prepare atlas300 driver and firmware

A300-3010-npu_20.1.0_ubuntu18.04-x86_64.zip

# unzip ,get the driver and firmware
A300-3010-npu-driver_20.1.0_ubuntu18.04-x86_64.run
A300-3010-npu-firmware_1.75.22.0.220.run

# create the username
```
useradd HwHiAiUser
usergroup -g HwHiAiUser -d /home/HwHiAiUser -m HwHiAiUser -s /bin/bash

passwd HwHiAiUser
```

# install the driver and firmware
 must install driver firstly
 according to the driver->firmware
## driver install

sudo ./A300-3010-npu-driver_20.1.0_ubuntu18.04-x86_64.run --full

## firmware install

sudo ./A300-3010-npu-firmware_1.75.22.0.220.run --full

## switch the user to verify

```
su HwHiAiUser

npu-smi info
```

# reference:
(Atlas 300I 推理卡 用户指南 型号:3010 13)[https://support.huawei.com/enterprise/zh/doc/EDOC1100079287/f9a811bc#ZH-CN_TOPIC_0252103982]

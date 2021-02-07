# 安装前准备

 根据instg-cli-cann.pdf的3.2.5章节进行配置
 
# 切换到root模式
sudo su

# 安装开发环境

./Ascend-cann-toolkit_20.1.rc1_linux-x86_64.run --install

# 运行环境
./Ascend-cann-nnrt_20.1.rc1_linux-x86_64 .run --install

# 实用工具包
./Ascend-mindstudio-toolbox_20.1.rc1_linux-x86_64.run --install

## 安装后环境变量的设置
参考instg-cli-cann.pdf的5.3.3章节
```
install_path=/usr/local/Ascend #请用户根据实际路径修改export PATH=${install_path}/toolbox/latest/Ascend-DMI/bin:${PATH}export LD_LIBRARY_PATH=/usr/local/dcmi:${install_path}/toolbox/latest/Ascend-DMI/lib64:${install_path}/nnrt/latest/acllib/lib64:/usr/local/Ascend/driver/lib64:${LD_LIBRARY_PATH}export PYTHONPATH=${install_path}/nnrt/latest/pyACL/python/site-packages/acl:$PYTHONPATH
```

# 在root模式下
`ascend-dmi info` 是否正确
`ascend-dmi -c` 检查驱动 固件 是否兼容
#参考
https://support.huaweicloud.com/instg-cli-cann/atlascli_03_0026.html
instg-cli-cann.pdf

doc/软件安装指南 (开发&运行场景, 通过命令行方式).pdf
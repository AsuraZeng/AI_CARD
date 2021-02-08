应用软件开发指南
https://support.huaweicloud.com/cann/
https://www.huaweicloud.com/ascend/resources/CodeSamples

成长地图:
01-软件安装
02-训练场景
03-推理场景

**atalas300(3010) 是推理,因此更加03推理场景**
# 应用开发
可以选用c/c++ 和python
接下来选用python作为开发

# env configruation

`sudo su` change to root mode

# ATC env setting

install_path= /usr/local/Ascend/ascend-toolkit/latest为例进行说明
```
export PATH=/usr/local/python3.7.5/bin:${install_path}/atc/ccec_compiler/bin:${install_path}/atc/bin:$PATH
export PYTHONPATH=${install_path}/atc/python/site-packages:${install_path}/atc/python/site-packages/auto_tune.egg/auto_tune:${install_path}/atc/python/site-packages/schedule_search.egg:$PYTHONPATH
export LD_LIBRARY_PATH=${install_path}/atc/lib64:$LD_LIBRARY_PATH
export ASCEND_OPP_PATH=${install_path}/opp
```
## actual env settings

add the below info to the ~/.bashrc 

referene:

```
install_path=/usr/local/Ascend
export PATH=${install_path}/toolbox/latest/Ascend-DMI/bin:/usr/local/python3.7.5/bin:${install_path}/ascend-toolkit/20.1.rc1/atc/ccec_compiler/bin:${install_path}/ascend-toolkit/20.1.rc1/atc/bin:${PATH}
export LD_LIBRARY_PATH=/usr/local/dcmi:${install_path}/toolbox/latest/Ascend-DMI/lib64:${install_path}/Ascend/nnrt/latest/acllib/lib64:/usr/local/Ascend/driver/lib64:${install_path}/nnrt/20.1.rc1/x86_64-linux/acllib/lib64:${install_path}/ascend-toolkit/20.1.rc1/atc/lib64:${LD_LIBRARY_PATH}
export PYTHONPATH=${install_path}/nnrt/latest/pyACL/python/site-packages/acl:${install_path}/ascend-toolkit/20.1.rc1/atc/python/site-packages:${install_path}/ascend-toolkit/20.1.rc1/atc/python/site-packages/auto_tune.egg/auto_tune:${install_path}/ascend-toolkit/20.1.rc1/atc/python/site-packages/schedule_search.egg:$PYTHONPATH
export ASCEND_OPP_PATH=${install_path}/ascend-toolkit/20.1.rc1/opp
```


# Python Demo execte

**I was in root mode**
sample path I have used:

`/usr/local/Ascend/nnrt/latest/pyACL/sample`

## 实现矩阵-矩阵相加运算

sample path:

`/usr/local/Ascend/nnrt/latest/pyACL/sample/acl_execute_op/acl_operator_add`

- change to root mode

- 在样例路径下执行如下命令,生成单算子模型文件

- 执行

`python3.7 acl_execute_add.py`




# reference

doc/应用软件开发指南（Python）.pdf


```
conda env list
# 列出所有环境

conda  create  --name  env_name python=3.9
# 创建python版本为3.9的虚拟环境

conda activate env_name
# 激活某个环境

conda deactivate
# 退出环境

conda  create  --name  new_env_name  --clone  old_env_name
# 复制某个环境

conda remove -n env_name --all
# 删除某个环境

conda  list  -n  env_name
# 查看这个环境的所有安装包

conda  install  xxx
# 进入虚拟环境后安装其他软件包

conda list
# 列出当下环境中所有包及其版本号
```

**Spyder是个python包，如果要在虚拟环境中运行spyder就只要conda install Spyder就可以了**



# link image0 hasn't been detected spyder，无法启动spyder

```
pip check

spyder 5.1.5 requires pyqt5, which is not installed.
spyder 5.1.5 requires pyqtwebengine, which is not installed.
autopep8 1.6.0 has requirement pycodestyle>=2.8.0, but you have pycodestyle 2.7.0.
# 显示缺少某些包

pip install pyqt5==5.12.3 -i https://pypi.tuna.tsinghua.edu.cn/simple
pip install pyqtwebengine==5.12.1 -i https://pypi.tuna.tsinghua.edu.cn/simple

pip uninstall pyzmq
pip install pyzmq==19.0.2 -i https://pypi.tuna.tsinghua.edu.cn/simple

spyder --new-instance
```

**即可解决！！！**


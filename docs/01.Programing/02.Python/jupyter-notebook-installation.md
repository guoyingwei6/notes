---
#title: Jupyter notebook下载与安装
tags:
  - python
---


## 安装

**不要用root用户pip install**

```shell
conda create -n python310 python==3.10
conda activate python310
conda install notebook

```

### 生成配置文件
```shell
jupyter notebook --generate-config
ipython
In [1]: from notebook.auth import passwd
In [2]: passwd()
# 可以直接回车输入空置，复制生成的密码值
vi /home/guoyingwei/.jupyter/jupyter_notebook_config.py
# 粘贴以下代码

c.NotebookApp.ip='*'                                                             
c.NotebookApp.password = u'argon2:$argon2id$v=19$m=10240,t=10,p=8$P4WMyf1ynxCOI168p50Gpg$xJmiOJ8V0St2QXXoayO9qQMG2ulDjR3/vf+UFViia9M'
c.NotebookApp.open_browser = False
c.NotebookApp.port=8888
c.NotebookApp.allow_remote_access = True

```


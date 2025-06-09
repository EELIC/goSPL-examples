
# WIN10 WSL2 Ubuntu 24.04.2 LTS 安装命令:

## 列出虚拟环境
```
conda env list
```

## 进入目录执行gospl1环境安装
```
cd goSPL-examples

conda env create -n gospl1 -f environment.yml 
```
## 安装 jupyter
```
conda install jupyter

```



## 安装失败->删除已安装gospl1环境
```
cd ~
conda remove -n gospl1 --all
```
修改 environment.yml

重复上述安装过程

## 运行 goSPL-examples
```
conda activate gospl1 
jupyter --version

```

回应输出:
```
Selected Jupyter core packages...
IPython          : 9.3.0
ipykernel        : 6.29.5
ipywidgets       : 8.1.7
jupyter_client   : 8.6.3
jupyter_core     : 5.8.1
jupyter_server   : 2.16.0
jupyterlab       : 4.4.3
nbclient         : 0.10.2
nbconvert        : 7.16.6
nbformat         : 5.10.4
notebook         : 7.4.3
qtconsole        : not installed
traitlets        : 5.14.3
```
## 在当前文件夹启动 Jupyter Notebook
```
cd ~/goSPL-examples/Local-examples/stratigraphic_record
jupyter notebook

```
## 浏览器打开
复制类似链接
```
http://localhost:8888/tree?token=504197a5aa32aca8b78794e66f6d8c2c1d1fdea8dad8d559
```

## 还有错误处理
 降级 numpy 到 1.23.x 或 1.24.x 的版本
```
conda install numpy=1.23.5
```

**激活虚拟环境**

```
激活基础环境
conda activate base
激活其他虚拟环境
conda activate name
```

**创建虚拟环境**

```
conda create --name myenv: 创建一个名为 myenv 的新环境。
conda create --name myenv python=3.8: 创建一个带有指定 Python 版本的环境。
conda create --name myenv numpy pandas: 创建一个包含指定软件包的环境。
```

**管理虚拟环境**

```
conda activate myenv: 激活名为 myenv 的环境。
conda deactivate: 停用当前环境。
conda env list: 列出所有可用环境。
-conda env remove --name myenv: 删除名为 myenv 的环境。
```



**安装、卸载、更新软件包**

```
conda install numpy: 安装 numpy 包。
conda install numpy=1.19.2: 安装指定版本的 numpy 包。
conda install --file requirements.txt: 从 requirements.txt 文件中安装所有指定的软件包。
conda remove numpy: 卸载 numpy 包。
conda update numpy: 更新 numpy 包到最新版本。
conda update --all: 更新所有已安装的软件包到最新版本。
conda search numpy: 搜索可用的 numpy 版本。
conda search "*search_term*": 在 Conda 存储库中搜索指定的软件包。
```




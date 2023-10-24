# conda

1. 查看
   ```shell
   conda --version              # 查看是否安装及当前版本
   conda list                   # 查看已安装的包
   conda env list               # 查看已创建的虚拟环境
   ```
2. 更新
   ```shell
   conda update conda           # 更新至最新版本 也会更新其它相关包
   conda update --all           # 更新所有包
   conda update package_name    # 更新指定的包
   ```
3. 虚拟环境
   ```shell
   conda create -n your_env_name python=x.x     # 创建虚拟环境
   conda activate your_env_name                 # Win 激活/切换虚拟环境
   conda deactivate                             # 关闭虚拟环境
   source activate you_env_name                 # Linux 激活/切换虚拟环境
   source deactivate                            # 关闭虚拟环境
   conda remove -n your_env_name --all          # 删除虚拟环境
   ```
4. 包
   ```shell
   conda install -n your_env_name [package]     # 安装包 环境外
   conda install [package]                      # 安装包 环境内
   ```
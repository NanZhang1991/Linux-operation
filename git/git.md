# 用户管理
## 配置用户名
```
git config user.name
git config user.email

git config --global user.name nanzhang1991
git config --global user.email nanzhang1991@gmail.com
```
## 记住用户密码
```
git config --global credential.helper store
```
# 代理
## 设置代理
ubuntu
```
git config --global http.proxy http://127.0.0.1:12333
git config --global https.proxy https://127.0.0.1:12333
git config --global http.proxy "socks5://127.0.0.1:12333"
```
windows
```
git config --global http.proxy http://127.0.0.1:1080
git config --global https.proxy https://127.0.0.1:1080
git config --global http.proxy "socks5://127.0.0.1:1080"
```

## 取消代理
```
git config --global --unset http.proxy
git config --global --unset https.proxy
```

## 查看config

##  查看系统config
```
git config --system --list
```

## 查看当前用户（global）配置
```
git config --global  --list
```

# git clone 加速
## 使用git shallow clone来下载
```
git clone https://github.com/xxx --depth 1
```

## 使用github cnpmjs镜像
```
git clone https://github.com/xxx.git
#改成：
git clone https://github.com.cnpmjs.org/xxx.git
```

# 创建与合并分支 ：

## 查看分支：
```
git branch
```
## 创建分支：
```
git branch <name>
```
## 切换分支：
```
git checkout <name>
```
## 创建+切换分支：
```
git checkout -b <name>
```
## 合并某分支到当前分支：
```
git merge <name>
```
## 删除分支：
```
git branch -d <name>
```
## 查看库中的文件状态
```
git status
```
## 对比文件修改过，但是还没有进行提交
```
git diff
git add fname
git commit -m 'add'
git pull
git push
```
## gitignore文件中忽略项不起作用的解决方法
```
git rm -r --cached .
git add .
git commit -m 'update .gitignore'
```
# Git submodul
submodule允许你将一个Git 仓库当作另外一个Git 仓库的子目录
## 添加子模块 
```bash
git submodule add https://git.apexsoft.com.cn/renerdong/docx-add-footnote.git
```
.gitmodules, 这个文件用来保存子模块的信息

## 查看子模块
```bash
git submodule
```
c4d713b98ae762dcd2e9bf82818731a22fcee743 app/docx-add-footnote (heads/main)

## 更新子模块
### 更新项目内子模块到最新版本
```bash
git submodule update
```
### 更新子模块为远程项目的最新版本
```
git submodule update --remote
```
## 克隆包含子模块的项目
递归克隆整个项目
```
git clone https://git.apexsoft.com.cn/forp/YFB/AI-GROUP/forp.footnote.service.git --recursive 
```
## 删除子模块
### 删除子模块文件夹
```
git rm --cached app/docx-add-footnote
rm -rf app/docx-add-footnote
```
### 删除.gitmodules文件中相关子模块信息
```
vim .gitmodules
```
[submodule "app/docx-add-footnote"]
	path = app/docx-add-footnote
	url = https://git.apexsoft.com.cn/renerdong/docx-add-footnote.git

### 删除.git/config中的相关子模块信息
```
vim .git/config
```
[submodule "app/docx-add-footnote"]
	url = https://git.apexsoft.com.cn/renerdong/docx-add-footnote.git
	active = true

### 删除.git文件夹中的相关子模块文件
rm -rf .git/modules/app/docx-add-footnote
=======
# 用户管理
## 配置用户名
```
git config user.name
git config user.email

git config --global user.name nanzhang1991
git config --global user.email nanzhang1991@gmail.com
```
## 记住用户密码
```
git config --global credential.helper store
```
# 代理
## 设置代理
ubuntu
```
git config --global http.proxy http://127.0.0.1:12333
git config --global https.proxy https://127.0.0.1:12333
```
windows
```
git config --global http.proxy http://127.0.0.1:1080
git config --global https.proxy https://127.0.0.1:1080
```

## 取消代理
```
git config --global --unset http.proxy
git config --global --unset https.proxy
```

## 查看config

##  查看系统config
```
git config --system --list
```

## 查看当前用户（global）配置
```
git config --global  --list
```

# git clone 加速
## 使用git shallow clone来下载
```
git clone https://github.com/xxx --depth 1
```

## 使用github cnpmjs镜像
```
git clone https://github.com/xxx.git
#改成：
git clone https://github.com.cnpmjs.org/xxx.git
```

# 创建与合并分支 ：

## 查看分支：
```
git branch
```
## 创建分支：
```
git branch <name>
```
## 切换分支：
```
git checkout <name>
```
## 创建+切换分支：
```
git checkout -b <name>
```
## 合并某分支到当前分支：
```
git merge <name>
```
## 删除分支：
```
git branch -d <name>
```
## 查看库中的文件状态
```
git status
```
## 对比文件修改过，但是还没有进行提交
```
git diff
git add fname
git commit -m 'add'
git pull
git push
```


# Git submodul
submodule允许你将一个Git 仓库当作另外一个Git 仓库的子目录
## 添加子模块 
```bash
git submodule add https://git.apexsoft.com.cn/renerdong/docx-add-footnote.git
```
.gitmodules, 这个文件用来保存子模块的信息

## 查看子模块
```bash
git submodule
```
c4d713b98ae762dcd2e9bf82818731a22fcee743 app/docx-add-footnote (heads/main)

## 更新子模块
### 更新项目内子模块到最新版本
```bash
git submodule update
```
### 更新子模块为远程项目的最新版本
```
git submodule update --remote
```
## 克隆包含子模块的项目
递归克隆整个项目
```
git clone https://git.apexsoft.com.cn/forp/YFB/AI-GROUP/forp.footnote.service.git --recursive 
```
## 删除子模块
### 删除子模块文件夹
```
git rm --cached app/docx-add-footnote
rm -rf app/docx-add-footnote
```
### 删除.gitmodules文件中相关子模块信息
```
vim .gitmodules
```
[submodule "app/docx-add-footnote"]
	path = app/docx-add-footnote
	url = https://git.apexsoft.com.cn/renerdong/docx-add-footnote.git

### 删除.git/config中的相关子模块信息
```
vim .git/config
```
[submodule "app/docx-add-footnote"]
	url = https://git.apexsoft.com.cn/renerdong/docx-add-footnote.git
	active = true

### 删除.git文件夹中的相关子模块文件
rm -rf .git/modules/app/docx-add-footnote
>>>>>>> 0e553f77842e6107364cd5a5e8ec951eda1d08d2

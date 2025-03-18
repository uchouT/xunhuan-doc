# 「寻寰」游戏设定站

主要是供开发使用，也有可能后续变成玩家维基，建设中 ...

## 如何编辑本页


### 前提

首先你要会使用 markdown 编辑，参考：[link](https://markdown.com.cn/basic-syntax/)。会基础编辑就够了，另外 gcd 可能要学会插入表格？

或者可以使用 Typora 来编辑 markdown 文件。我站里有破解版：[link](https://drive.uchout.moe/d/App/typora_64bit_v1.9.5_setup.rar)

### 1. 克隆仓库

仓库地址：[GitHub](github.com/uchouT/xunhuan-doc)

在本地安装 [Git](https://git-scm.com/downloads), 然后克隆本仓库的 main 分支到本地，然后在项目中的 /docs 文件夹中即可找到 markdown 文件进行编辑~

侧栏的导航菜单在 mkdocs.yml 中编辑。

### 2. 推送部署网页

我在 main 分支设置了 GitHub workflows，可以自动部署，因此不需要手动修改 gh-deploy 分支。

所以很简单，在写作完成之后，运行 `git push origin main` 即可。
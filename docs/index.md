# 「寻寰」游戏设定站

主要是供开发使用，也有可能后续变成玩家维基，建设中 ...

## ToDo

- 目前**优先**需要完善的地方是各种属性，需要注意的是，属性要非常细致，但是不需要具体，举例来说，「细致」表示：不仅需要物理、魔法等战斗属性，还需要比如价格、系别等等一切；而「不需要具体」表示：目前暂时先不用设计具体的数值，比如价格是多少，物理值是多少。这些以后考虑，目前我想先把类搞出来。总之，尽可能全面的完善属性（角色，武器，地图，etc. )
- 各种机制，这个慢慢来，要写机制需要先有类，可以与属性结合着来考虑，比如你引入远程、近战的攻击机制，那么相应的，属性就得有这一项。

## 如何编辑本页

### 前提

1. 首先你要会使用 markdown 编辑，参考：[link](https://markdown.com.cn/basic-syntax/)。会基础编辑就够了，另外 gcd 可能要学会插入表格？

或者可以使用 Typora 来编辑 markdown 文件。我站里有破解版：[link](https://drive.uchout.moe/d/App/typora_64bit_v1.9.5_setup.rar)

2. 有一个 GitHub 账号，并且告诉我用户名，我来添加推送权限。

### 1. 克隆仓库

仓库地址：[GitHub](github.com/uchouT/xunhuan-doc)

在本地安装 [Git](https://git-scm.com/downloads), 然后克隆本仓库的 main 分支到本地，然后在项目中的 /docs 文件夹中即可找到 markdown 文件进行编辑~

**WARNING：**在每次编辑之前，先运行 `git pull origin main` ， 将远程仓库拉取到本地，以防止有人做了文档修改而本地没有及时更新。

侧栏的导航菜单在 `mkdocs.yml` 中编辑。

### 2. 推送部署网页

我在 main 分支设置了 GitHub workflows，可以自动部署，因此不需要手动修改 gh-deploy 分支。

所以很简单，在写作完成之后，运行 `git push origin main` 即可。

没有设置 ssh 密钥的话要先设置，在电脑 (windows) 的 `C:\Users\你的用户名\.ssh` 路径找找有没有 `id_rsa.pub` 或者类似 `*.pub` 的文件，如果没有的话，打开 git-bash，输入 `ssh-keygen -t rsa -b 4096 -C "你的邮箱@example.com"` 生成一下，然后将 `.pub` 文件中的内容添加到 GitHub 账号中：[New SSH Key](https://github.com/settings/keys)
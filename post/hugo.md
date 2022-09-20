title: "meme主题"
date: 2022-09-20
tags: ["tips"]
categories: ["生活"]

meme主题搭建

### hugo安装

下载hugo https://github.com/gohugoio/hugo/releases/
环境变量：ln -s xx/xx/xx/hugo /usr/local/bin/hugo
hugo new site klearblog	##创建站点根目录

### meme主题下载

hugo不自带主题，俺选择meme
进入klearblog目录	git clone https://github.com/reuixiy/hugo-theme-meme.git themes/meme	##直接cp下来:dog2:	（问题：安装了git却无限安装。原因：系统更新解决：进xcode更新）
hugo new post/a.md	##创建个文件测试下
echo asdasdasd >> content/post/a.md   ##文件内追加点东西
Hugo server -v -D 	 	##本地看下效果,根据提示http://localhost:1313

### 提交至github

新建仓库->命名为 名字.github.io->选择public->点击创建 即可创建仓库
来到博客根目录(klearblog) 执行Hugo -D 生成所需数据
进入public目录，执行
git init 
git remote add origin git@github.com:Klearcc/Klearcc.github.io.git
git add .
git commit -m"test"
git push --set-upstream origin main
(其中可能遇到各种问题，尤其在重复提交情况下，根据报错自行百度根据前辈建议操作即可解决)

### ssh公钥配置

自行百度

### 效果

项目->设置->pages，点击预览站点即可。

### 后续文章变更：

git init
Git add .
Git commit -m"123"
git push
为了方便（写个sh或githubdesktop）

### Typora提交图片问题

问题：自己截的图片提交时候不会自动提交到github上。
解决：typora+picgo
新建一个放图片的仓库，比如命名为pic
typora21年某个版本之后支持图床，选择Picgo

![image-20220920203722221](https://cdn.jsdelivr.net/gh/klearcc/pic/imgs202209202037266.png)picgo配置，仓库名为 名字+pic，
设置token：github设置-developer settings
存储路径随意设置
自定义域名为jsdelivrCDN，填写规则如图：

![image-20220920203832229](https://cdn.jsdelivr.net/gh/klearcc/pic/imgs202209202038248.png)
![image-20220920203916950](https://cdn.jsdelivr.net/gh/klearcc/pic/imgs202209202039972.png)


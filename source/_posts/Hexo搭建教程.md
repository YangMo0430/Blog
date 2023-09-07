---
title: Hexo搭建教程
date: 2023-09-07 14:36:58
tags:
- Hexo
- Linux
categories: 常用工具
---

# 环境配置

```
brew install node
npm install hexo-cli -g # 全局安装hexo命令行工具
```

```
hexo init Blog
cd Blog
npm install
```

```
# 在package.json 中添加脚本：
"netlify": "npm run clean && npm run build"
# 后续在netlify中修改Build Command为：
npm run netlify
```
# 主题配置
## 下载
```
git clone -b master https://github.com/jerryc127/hexo-theme-butterfly.git themes/butterfly

# 安装插件
npm install hexo-renderer-pug hexo-renderer-stylus --save
```

**主题下载下来后主题的 .git 文件夹删掉，不要用子模块！**

修改_config.yml：theme: butterfly

复制themes/butterfly中的_config.yml并改名为_config.butterfly.yml
## 本地测试
```
hexo new post "test" # 会在 source/_posts/ 目录下生成文件 ‘test.md’，打开编辑  
hexo generate        # 生成静态HTML文件到 /public 文件夹中  
hexo server          # 本地运行server服务预览，打开          http://localhost:4000 即可预览你的博客
```
## git创建仓库&远程推送
```
cd "Blog"  
git init  #初始化仓库。
git add .  #添加文件到暂存区。
git commit -m "my blog first commit"  #提交暂存区到本地仓库。

git remote add origin git@github.com:YangMo0430/Blog.git
git branch -M main
git push -u origin main
```
# Netlify建站
# Errors
```
extends includes/layout.pug block content include ./includes/mixins/post-ui.pug #recent-posts.recent-posts +postUI include includes/pagination.pug
```

```
npm install hexo-renderer-pug hexo-renderer-stylus --save
```

```
11:56:55 AM: Failed during stage 'preparing repo': Error checking out submodules: fatal: No url found for submodule path 'themes/butterfly' in .gitmodules  
: exit status 128: fatal: No url found for submodule path 'themes/butterfly' in .gitmodules
```

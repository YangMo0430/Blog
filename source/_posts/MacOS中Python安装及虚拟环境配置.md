---
title: Python开发工具
date: 2023-07-14 13:23:54
tags: 
- Python
- MacOS
categories: Python
---

# Python安装（Mac OS）

- 安装Xcode命令行工具
  ```xcode-select --install```

- 安装homebrew

- 安装python3和pip3
  ```brew install python```

# Pipenv使用方法

### 安装Pipenv

- 检查Python和pip
  ```python --version```
  ```pip --version```

- 安装pipenv
  ```pip install --user pipenv```
  
- （如果报错shell找不到命令）全局安装
  
  ```pip3 uninstall pipenv```
  
  ```sudo -H pip3 install -U pipenv```

### 创建虚拟环境

- ```mkdir ProjectName```
- ```cd ProjectName```
- ```pipenv install```
- ```pipenv install jupyter matplotlib numpy pandas scikit-learn scipy```

### 常用命令

- ```pipenv shell```
- ```exit```
- 



# Python 开发环境

# 写出优雅的Python代码

## 结构化


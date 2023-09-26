---
title: The Hitchhiker's Guide to Python
date: 2023-09-25 13:23:54
tags: 
- Python
- MacOS
categories: Python
---

# Part1 Getting Started

## About Python

### Implementations

- CPython
- Stackless
- PyPy
- Jython
- IronPython
- PythonNet
- Skulpt
- MicroPython

### Developent Tools

- Concurrency tools
  - threading
  - asyncio
  - curio
  - gevent
  - Twisted

- Scientific analysis
  - NumPy
  - SciPy
  - scikit-learn
  - Matplotlib

- Data/database interface
  - h5py
  - Psycopg
  - SQLAlchemy

## Python安装（Mac OS）

- 安装Xcode命令行工具
  ```xcode-select --install```

- 安装homebrew

- 安装python3和pip3
  ```brew install python```
  
- 更新pip
  
  ```pip3 install --upgrade pip```

## Pipenv使用方法

[Pipenv & 虚拟环境 — The Hitchhiker's Guide to Python (pythonguidecn.readthedocs.io)](https://pythonguidecn.readthedocs.io/zh/latest/dev/virtualenvs.html)

### 安装Pipenv

- 检查Python和pip
  ```python --version```
  ```pip --version```

- 安装pipenv
  ```pip install --user pipenv```
  
  ```pip install --upgrade pip```
  
- （如果报错shell找不到命令）全局安装
  
  ```pip3 uninstall pipenv```
  
  ```sudo -H pip3 install -U pipenv```

### 创建虚拟环境

- ```mkdir ProjectName```
- ```cd ProjectName```
- ```pipenv install```
- ```pipenv install jupyter matplotlib numpy pandas scikit-learn scipy```

### 常用命令

- 激活虚拟环境```pipenv shell```
- 运行脚本```pipenv run python main.py```
- 退出```exit```

### 自动记录依赖

- Pipfile用来记录项目依赖包列表，而Pipfile.lock记录了固定版本的详细依赖包列表。

### 更改项目虚拟环境文件位置

- ```export WORKON_HOME=PIPENV_VENV_IN_PROJECT```

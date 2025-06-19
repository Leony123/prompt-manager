# Prompt Manager

Prompt Manager 是一个基于 Django 的提示词管理系统，帮助用户高效管理和组织 AI 提示词。系统提供了直观的界面，支持提示词的创建、编辑、分类和搜索等功能。

## 功能特性
测试
- 用户管理
  - 用户注册和登录
  - 个人提示词管理
  - 权限控制

- 提示词管理
  - 创建和编辑提示词
  - 版本控制
  - 标签分类
  - 复制到剪贴板
  - 搜索和过滤

- 标签系统
  - 创建和管理标签
  - 标签分类
  - 公共/私有标签

- 界面特性
  - 响应式设计
  - 现代化 UI
  - 实时搜索
  - 复制成功提示
  - 编辑模式切换

## 技术栈

- 后端：Django 4.2
- 数据库：SQLite3
- 前端：
  - Bootstrap 5
  - jQuery
  - Select2
  - Bootstrap Icons

## 环境要求

- Python 3.11
- pip（Python 包管理器）
- 虚拟环境（推荐）

## 安装步骤

1. 克隆项目
```bash
git clone [项目地址]
cd prompt-manager
```

2. 创建并激活虚拟环境
```bash
python -m venv venv
source venv/bin/activate  # Linux/Mac
# 或
.\venv\Scripts\activate  # Windows
```

3. 安装依赖
```bash
pip install django==4.2
```

4. 初始化数据库
```bash
python manage.py makemigrations
python manage.py migrate
```

5. 创建超级用户（可选）
```bash
python manage.py createsuperuser
```

6. 运行开发服务器
```bash
python manage.py runserver
```

## 使用说明

1. 访问系统
   - 开发环境：http://localhost:8000
   - 登录页面：http://localhost:8000/login/

2. 主要功能
   - 提示词列表：查看所有提示词
   - 创建提示词：点击"新建提示词"按钮
   - 编辑提示词：点击提示词卡片上的编辑按钮
   - 复制提示词：点击复制按钮，内容会自动复制到剪贴板
   - 标签管理：创建和管理标签
   - 搜索：使用搜索框快速查找提示词

3. 提示词管理
   - 创建新提示词时填写标题、内容和描述
   - 可以为提示词添加标签
   - 支持版本控制
   - 可以设置提示词为公开或私有

## 开发说明

1. 项目结构
```
prompt-manager/
├── manage.py
├── promptmanager/      # 项目配置
├── prompts/           # 主应用
│   ├── models.py     # 数据模型
│   ├── views.py      # 视图
│   ├── urls.py       # URL 配置
│   └── templates/    # 模板文件
└── db.sqlite3        # 数据库文件
```

2. 主要模型
   - User：用户模型
   - Prompt：提示词模型
   - Tag：标签模型

## 部署说明

1. 生产环境配置
   - 修改 settings.py 中的 DEBUG = False
   - 配置 ALLOWED_HOSTS
   - 设置 SECRET_KEY
   - 配置静态文件服务

2. 数据库迁移
   - 建议使用 PostgreSQL 等生产级数据库
   - 更新 DATABASES 配置

3. 静态文件收集
```bash
python manage.py collectstatic
```

4. 使用生产级服务器
   - 推荐使用 Gunicorn 或 uWSGI
   - 配置 Nginx 作为反向代理

## 贡献指南

1. Fork 项目
2. 创建特性分支
3. 提交更改
4. 推送到分支
5. 创建 Pull Request

## 许可证

[添加许可证信息]

## 联系方式

[添加联系方式] 
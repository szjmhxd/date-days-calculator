# 天数计算器

一个简洁美观的天数计算器，支持计算从指定日期到当前日期的天数，以及特殊天数的计算。

## 功能特点

1. **天数计算**：从指定日期计算到当前日期的天数
2. **默认日期快速选择**：支持添加、选择默认日期
3. **特殊日期计算**：自动计算指定日期的第N天
4. **多主题支持**：支持8种不同风格的主题切换
5. **响应式设计**：适配不同屏幕尺寸
6. **本地存储**：默认日期和特殊天数存储在本地

## 文件结构

```
.
├── index.html          # 主页面
├── settings.html       # 默认日期设置页面
├── special-days.html   # 特殊天数设置页面
└── README.md           # 项目说明文档
```

## 使用方法

### 基本使用

1. 在主页面选择起始日期
2. 点击"计算天数"按钮查看结果
3. 结果将显示从起始日期到当前日期的天数

### 快速选择默认日期

1. 在主页面的"快速选择默认日期"下拉菜单中选择预设日期
2. 点击"应用"按钮将该日期设置为起始日期
3. 点击"+ 新增"按钮进入设置页面添加新的默认日期

### 管理特殊天数

1. 点击"管理特殊天数"链接进入特殊天数设置页面
2. 添加、编辑或删除要计算的特殊天数
3. 返回主页面，计算结果将显示这些特殊天数对应的日期

### 切换主题

1. 点击右下角的主题切换按钮
2. 从弹出的主题选择面板中选择喜欢的主题
3. 页面将立即应用所选主题

## 部署方法

### 普通部署

1. **准备服务器**
   - 购买并登录云服务器（如阿里云、腾讯云、华为云等）
   - 安装Web服务器软件（Apache或Nginx）

2. **安装Web服务器**

   #### 对于Ubuntu/Debian系统
   ```bash
   # 更新软件包列表
   sudo apt update
   
   # 安装Apache
   sudo apt install apache2
   
   # 或安装Nginx
   sudo apt install nginx
   ```

   #### 对于CentOS/RHEL系统
   ```bash
   # 更新软件包列表
   sudo yum update
   
   # 安装Apache
   sudo yum install httpd
   
   # 或安装Nginx
   sudo yum install nginx
   ```

3. **启动Web服务器**

   #### Apache
   ```bash
   # Ubuntu/Debian
   sudo systemctl start apache2
   sudo systemctl enable apache2
   
   # CentOS/RHEL
   sudo systemctl start httpd
   sudo systemctl enable httpd
   ```

   #### Nginx
   ```bash
   # Ubuntu/Debian
   sudo systemctl start nginx
   sudo systemctl enable nginx
   ```

4. **上传文件**
   - 将项目文件上传到Web服务器的根目录
   - Apache默认根目录：`/var/www/html/`
   - Nginx默认根目录：`/usr/share/nginx/html/`

   ```bash
   # 使用scp命令上传文件
   scp -r * username@your-server-ip:/var/www/html/
   ```

5. **访问网站**
   - 在浏览器中输入服务器IP地址或域名
   - 如：`http://your-server-ip/`

### 宝塔部署

1. **安装宝塔面板**
   - 登录云服务器
   - 执行宝塔面板安装命令
   
   ```bash
   # CentOS系统
   yum install -y wget && wget -O install.sh http://download.bt.cn/install/install_6.0.sh && sh install.sh
   
   # Ubuntu/Debian系统
   wget -O install.sh http://download.bt.cn/install/install-ubuntu_6.0.sh && sudo bash install.sh
   ```

2. **登录宝塔面板**
   - 安装完成后，会显示宝塔面板的登录地址、用户名和密码
   - 在浏览器中输入登录地址，使用提供的用户名和密码登录

3. **创建网站**
   - 登录宝塔面板后，点击左侧菜单"网站" -> "添加站点"
   - 填写域名（或IP地址）、根目录等信息
   - 点击"提交"创建网站

4. **上传文件**
   - 点击创建的网站右侧的"文件"
   - 进入网站根目录
   - 点击"上传"按钮，将项目文件上传到根目录

5. **访问网站**
   - 在浏览器中输入您设置的域名或IP地址
   - 如：`http://your-domain.com/` 或 `http://your-server-ip/`

## 主题说明

支持以下8种主题：

1. **默认紫**：紫色渐变背景
2. **简洁白**：白色简约风格
3. **少女粉**：粉色渐变背景
4. **主题黑**：深色主题
5. **高能红**：红色渐变背景
6. **咸蛋黄**：黄色渐变背景
7. **早苗绿**：绿色渐变背景
8. **宝石蓝**：蓝色渐变背景（默认）

## 技术栈

- HTML5
- CSS3（包括CSS变量、渐变、动画等）
- JavaScript（原生JS，无需依赖库）

## 浏览器兼容性

支持所有现代浏览器：
- Chrome (推荐)
- Firefox
- Safari
- Edge

## 本地开发

1. 在本地创建项目目录
2. 将文件放入该目录
3. 使用本地HTTP服务器运行项目

   ```bash
   # 使用Python 3
   python -m http.server 8000
   
   # 使用Node.js（需安装http-server）
   npx http-server -p 8000
   ```

4. 在浏览器中访问 `http://localhost:8000`

## 许可证

本项目采用MIT许可证，可自由使用和修改。
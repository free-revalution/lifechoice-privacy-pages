# LifeChoice 隐私与服务页面

## 项目概述

本目录包含LifeChoice应用的隐私政策、用户服务协议和技术支持页面的HTML文件。这些页面用于满足App Store上架要求，支持中文和英文双语版本。

## 页面结构

```
app-privacy-page/
├── index.html           # 首页（导航页）
├── privacy-policy-zh.html   # 中文隐私政策
├── privacy-policy-en.html   # 英文隐私政策
├── terms-of-service-zh.html # 中文用户服务协议
├── terms-of-service-en.html # 英文用户服务协议
├── support-zh.html      # 中文技术支持
├── support-en.html      # 英文技术支持
└── README.md            # 本说明文件
```

## 使用方法

### 本地预览

在部署到GitHub Pages之前，您可以在本地预览这些页面：

1. 打开终端
2. 进入`app-privacy-page`目录
3. 运行本地服务器：
   
   ```bash
   # 使用Python 3
   python -m http.server 8000
   
   # 或使用Node.js的http-server
   npx http-server -p 8000
   ```

4. 在浏览器中访问`http://localhost:8000`

### 部署到GitHub Pages

按照以下步骤将页面部署到GitHub Pages：

#### 1. 创建GitHub仓库

1. 登录GitHub账号
2. 点击右上角的"+"图标，选择"New repository"
3. 填写仓库信息：
   - Repository name: 可以使用 `lifechoice-privacy-pages` 或其他名称
   - Description: 可选，描述仓库用途
   - Visibility: 选择"Public"（GitHub Pages要求公共仓库）
4. 点击"Create repository"

#### 2. 上传文件到仓库

有两种方式可以上传文件：

##### 方式一：使用Git命令行

1. 在本地`app-privacy-page`目录初始化Git仓库：
   
   ```bash
   cd /Users/jiang/development/LifeChoice/app-privacy-page
   git init
   ```

2. 连接到GitHub仓库：
   
   ```bash
   git remote add origin https://github.com/[your-username]/[repository-name].git
   ```

3. 提交并推送文件：
   
   ```bash
   git add .
   git commit -m "Initial commit: Add privacy policy pages"
   git push -u origin master
   ```

##### 方式二：通过GitHub网页上传

1. 进入您创建的GitHub仓库
2. 点击"Add file"按钮，选择"Upload files"
3. 拖拽`app-privacy-page`目录下的所有文件到上传区域
4. 填写提交信息，点击"Commit changes"

#### 3. 启用GitHub Pages

1. 进入GitHub仓库的"Settings"页面
2. 在左侧菜单中选择"Pages"
3. 在"Source"部分：
   - 选择分支：`master`（或`main`，取决于您的默认分支名称）
   - 选择目录：`/ (root)`
4. 点击"Save"
5. 等待几分钟，GitHub Pages将部署您的网站
6. 部署完成后，您将看到一个绿色的通知，显示您的网站URL（格式：`https://[your-username].github.io/[repository-name]/`）

### 配置App Store连接

部署完成后，您需要在App Store Connect中配置隐私政策和技术支持的URL：

1. 登录App Store Connect
2. 选择您的App
3. 进入"App Information"页面
4. 在"Privacy Policy URL"字段中填写隐私政策页面的URL（例如：`https://[your-username].github.io/[repository-name]/privacy-policy-zh.html`）
5. 在"Technical Support URL"字段中填写技术支持页面的URL（例如：`https://[your-username].github.io/[repository-name]/support-zh.html`）
6. 保存更改

## 自定义内容

您可以根据需要修改HTML文件中的以下内容：

1. **开发者信息**：将所有`[开发者姓名/个人开发者]`和`[Developer Address]`替换为您的真实信息
2. **联系方式**：确保`feedback@lifechoice.app`是您的有效邮箱地址
3. **日期**：检查并更新所有文档的生效日期和最后更新日期

## 技术说明

- 所有页面都使用响应式设计，适配不同屏幕尺寸
- 页面支持中英文双语切换
- 使用纯HTML和CSS实现，无需额外依赖
- 符合App Store上架要求的隐私政策和技术支持页面标准

## 更新与维护

当您需要更新隐私政策或其他页面时：

1. 修改本地HTML文件
2. 按照上述Git命令行步骤提交并推送更改
3. GitHub Pages将自动更新网站内容
4. 更新App Store Connect中的URL（如果页面路径发生变化）

## 注意事项

- 确保所有页面的URL在App Store Connect中正确配置
- 定期检查并更新隐私政策以符合最新的法律法规要求
- 确保技术支持页面提供有效的联系方式
- GitHub Pages网站通常需要几分钟时间来更新新内容

## 联系方式

如有任何问题，请联系：
- Email: feedback@lifechoice.app
# lifechoice-privacy-pages

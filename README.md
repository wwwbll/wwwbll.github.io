# 王大状律师 - 个人展业网页

一个专业的律师个人展业单页网站，可直接部署到 GitHub Pages 免费托管。

## 功能特点

- 响应式设计，完美适配手机/平板/电脑
- 深蓝主色调，专业沉稳
- 中英双语展示
- 6大区块：首页、关于我、专业领域、专业成就、经典案例、联系方式
- 滚动渐入动画、数字滚动效果
- 服务卡片可展开/收起
- 浮动联系按钮 + 弹窗
- 纯静态 HTML，无需后端服务器

## GitHub Pages 部署步骤

### 1. 创建 GitHub 仓库

1. 登录 [GitHub](https://github.com)
2. 点击右上角 "+" → "New repository"
3. 仓库名建议填写：`lawyer-website`（或其他你喜欢的名字）
4. 设为 **Public**（GitHub Pages 免费版要求公开仓库）
5. 点击 "Create repository"

### 2. 上传代码

方式一：网页上传
1. 在仓库页面点击 "uploading an existing file"
2. 将本项目文件夹中的所有文件拖入上传
3. 点击 "Commit changes"

方式二：命令行上传
```bash
cd lawyer-website
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/你的用户名/lawyer-website.git
git push -u origin main
```

### 3. 开启 GitHub Pages

1. 进入仓库 → Settings → Pages
2. Source 选择 "Deploy from a branch"
3. Branch 选择 `main`，文件夹选 `/ (root)`
4. 点击 Save
5. 等待 1-2 分钟，页面顶部会出现你的网站地址：
   `https://你的用户名.github.io/lawyer-website/`

## 自定义内容

打开 `index.html`，搜索以下关键词替换为你的真实信息：

| 搜索内容 | 替换为 |
|---------|--------|
| `王大状` | 你的姓名 |
| `专职律师 · 法律类内容创作者` | 你的身份描述 |
| `your.email@example.com` | 你的邮箱 |
| `your_wechat_id` | 你的微信号 |
| `请填写你的办公地址` | 你的办公地址 |
| `形象照` 占位区域 | 替换为 `<img src="你的照片URL" alt="形象照">` |

### 替换形象照

找到 Hero 区域的占位 div，替换为：
```html
<img src="photo.jpg" alt="律师形象照" class="w-full h-auto object-cover">
```
将照片文件放在同目录下即可。

## 技术栈

- TailwindCSS（通过 CDN 引入）
- 纯原生 HTML + CSS + JavaScript
- 无需构建工具，无需安装依赖

## 文件结构

```
lawyer-website/
├── index.html      ← 主网页文件（所有内容都在这里）
├── README.md       ← 本说明文件
└── .gitignore      ← Git 忽略配置
```

## 浏览器兼容

支持所有现代浏览器：Chrome、Firefox、Safari、Edge 等。

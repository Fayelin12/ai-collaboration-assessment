# 🚀 发布到 GitHub Pages - 完整指南

## 📋 准备工作

### 1. 创建 GitHub 账号（如果没有）
- 访问 [github.com](https://github.com)
- 点击 "Sign up" 注册免费账号

---

## 🔧 方法一：使用 Git 命令行（推荐）

### 步骤 1：打开项目目录
```bash
cd "G:\桌面"
```

### 步骤 2：初始化 Git 仓库
```bash
git init
```

### 步骤 3：添加 HTML 文件
```bash
git add AI 协作成熟度评估.html
```

### 步骤 4：提交文件
```bash
git commit -m "🎉 发布 AI 协作成熟度评估工具"
```

### 步骤 5：创建 GitHub 仓库
1. 访问 https://github.com/new
2. **Repository name**: `ai-collaboration-assessment`
3. **Description**: `AI 协作成熟度评估工具 - 基于 Anthropic AI Fluency Framework`
4. **选择**: ✅ Public（公开）
5. ❌ 不要勾选 "Add a README file"
6. ❌ 不要勾选 "Add .gitignore"
7. ❌ 不要勾选 "Choose a license"
8. 点击 **"Create repository"**

### 步骤 6：关联远程仓库
复制页面上显示的命令（替换 YOUR_USERNAME 为你的 GitHub 用户名）：
```bash
git remote add origin https://github.com/YOUR_USERNAME/ai-collaboration-assessment.git
git branch -M main
git push -u origin main
```

### 步骤 7：启用 GitHub Pages
1. 在你的仓库页面，点击 **Settings**
2. 左侧菜单找到并点击 **Pages**
3. **Source** 选择：`Deploy from a branch`
4. **Branch** 选择：`main` 
5. **Folder** 选择：`/ (root)`
6. 点击 **Save**

### 步骤 8：等待部署完成
- 等待 1-2 分钟
- 刷新 Pages 设置页面
- 你会看到类似这样的链接：
  ```
  https://YOUR_USERNAME.github.io/ai-collaboration-assessment/
  ```

### 🎉 完成！
现在你可以把这个链接分享给任何人访问了！

---

## 🖱️ 方法二：使用 GitHub Desktop（图形界面）

### 步骤 1：下载 GitHub Desktop
- 访问 https://desktop.github.com
- 下载并安装

### 步骤 2：登录 GitHub Desktop
- 打开应用
- 使用 GitHub 账号登录

### 步骤 3：添加项目
1. 点击 **File → Add Local Repository**
2. 选择 `G:\桌面` 文件夹
3. 点击 **Add repository**

### 步骤 4：首次提交
1. 在 Changes 标签页，勾选 `AI 协作成熟度评估.html`
2. 填写摘要：`发布 AI 协作成熟度评估工具`
3. 点击 **Commit to main**

### 步骤 5：发布到 GitHub
1. 点击右上角 **Publish repository**
2. 填写名称：`ai-collaboration-assessment`
3. ✅ 勾选 "Keep this code private"（如果需要私有）
4. 点击 **Publish repository**

### 步骤 6：启用 Pages
同上，在 Settings → Pages 中启用。

---

## 📊 高级选项

### 自定义域名（可选）
如果你想用自己的域名：

1. 在 Pages 设置中找到 **Custom domain**
2. 输入你的域名，如：`assessment.yourdomain.com`
3. 按照提示配置 DNS
4. 点击 **Save**

### 自动部署工作流
创建 `.github/workflows/deploy.yml`：

```yaml
name: Deploy to GitHub Pages

on:
  push:
    branches: [main]

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      
      - name: Deploy to GitHub Pages
        uses: peaceiris/actions-gh-pages@v3
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          publish_dir: ./
```

---

## ❓ 常见问题

### Q: 上传后看不到页面？
A: 等待 1-2 分钟，GitHub 需要时间构建和部署。

### Q: 如何更新内容？
A: 修改 HTML 文件后，重新执行：
```bash
git add AI 协作成熟度评估.html
git commit -m "更新评估工具"
git push
```

### Q: 如何查看访问统计？
A: 在仓库的 **Insights → Traffic** 中查看。

### Q: 可以多人协作吗？
A: 可以！邀请其他人成为仓库协作者即可。

---

## 📞 需要帮助？

如果遇到任何问题：
1. 检查 GitHub Status: https://www.githubstatus.com
2. 查看 GitHub Docs: https://docs.github.com/en/pages
3. 或者在仓库中提 Issue

---

**祝你部署顺利！** 🎊

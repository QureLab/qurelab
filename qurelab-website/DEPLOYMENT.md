# QureLab Website Deployment Guide

## GitHub Pages 部署说明

### 1. 推送代码到 GitHub

首先，将项目推送到 GitHub 仓库：

```bash
git init
git add .
git commit -m "Initial commit: QureLab website"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/qurelab-website.git
git push -u origin main
```

### 2. 启用 GitHub Pages

1. 进入 GitHub 仓库设置页面
2. 滚动到 "Pages" 部分
3. 在 "Source" 下选择 "GitHub Actions"

### 3. 自动部署

项目已配置了 GitHub Actions 工作流（`.github/workflows/deploy.yml`），当代码推送到 `main` 分支时会自动：

- 安装依赖
- 构建项目
- 部署到 GitHub Pages

### 4. 访问网站

部署完成后，网站将在以下地址可用：
```
https://YOUR_USERNAME.github.io/qurelab-website/
```

### 5. 本地开发

```bash
# 安装依赖
npm install

# 启动开发服务器
npm run dev

# 构建生产版本
npm run build

# 预览构建结果
npm run preview
```

### 注意事项

- 确保仓库名为 `qurelab-website`，或者修改 `vite.config.ts` 中的 `base` 配置
- GitHub Pages 可能需要几分钟时间来部署更新
- 首次部署可能需要等待 GitHub Actions 工作流完成

### 设计特色

- 极简主义设计语言
- 黑白灰色调配色方案
- 响应式布局
- 现代 Vue 3 + TypeScript 技术栈
- 数据可视化元素
- 专业的排版和间距
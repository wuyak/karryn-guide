# Karryn's Prison 游戏攻略 - GitHub Pages 部署

本仓库用于部署繁简双语版游戏攻略到 GitHub Pages。

## 📁 目录结构

```
deploy_karryn/
├── docs/              # 繁体版（zh-TW）
├── docs-cn/           # 简体版（zh-CN）
├── package.json       # VitePress 依赖配置
└── .github/
    └── workflows/
        └── deploy.yml # 自动部署脚本
```

## 🚀 部署步骤

### 1. 创建 GitHub 仓库

1. 在 GitHub 创建新仓库（例如：`karryn-guide`）
2. 不要初始化 README

### 2. 上传代码

```bash
cd "F:\ready to go\deploy_karryn"
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/你的用户名/karryn-guide.git
git push -u origin main
```

### 3. 启用 GitHub Pages

1. 进入仓库 Settings → Pages
2. Source 选择：**GitHub Actions**
3. 保存

### 4. 自动部署

推送代码后，GitHub Actions 会自动：
1. 安装依赖
2. 构建繁体版和简体版
3. 部署到 GitHub Pages

## 🌐 访问地址

部署完成后：

- **繁体版**：`https://你的用户名.github.io/karryn-guide/`
- **简体版**：`https://你的用户名.github.io/karryn-guide/cn/`

## 💻 本地预览

```bash
# 安装依赖
npm install

# 预览繁体版
npm run docs:dev

# 预览简体版
npm run docs-cn:dev

# 手动构建
npm run build
```

## 📝 更新内容

从原项目更新内容后：

```bash
# 在原项目目录
cd "F:\ready to go\卡琳的监狱攻略整理工具"

# 复制更新的文件
cp -r docs/* "../deploy_karryn/docs/"
cp -r docs-cn/* "../deploy_karryn/docs-cn/"

# 提交并推送
cd "../deploy_karryn"
git add .
git commit -m "Update content"
git push
```

## ⚙️ 技术栈

- [VitePress](https://vitepress.dev/) - 静态站点生成器
- GitHub Actions - 自动化部署
- GitHub Pages - 静态网站托管

## 📄 许可

内容来源于巴哈姆特论坛，原作者：黑巧
仅供学习交流使用，请勿用于商业用途

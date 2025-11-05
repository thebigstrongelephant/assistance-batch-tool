# 🚀 GitHub Pages 部署指南

本指南将帮助你将乡村公益平台项目部署到GitHub Pages。

## 📋 部署步骤

### 1. 创建GitHub仓库

1. 登录 [GitHub](https://github.com)
2. 点击右上角的 "+" 按钮，选择 "New repository"
3. 仓库名称建议使用：`rural-charity-platform`
4. 设置为 Public（GitHub Pages 免费版需要公开仓库）
5. 不要初始化 README、.gitignore 或 license（因为本地已有）

### 2. 推送代码到GitHub

在项目根目录执行以下命令：

```bash
# 如果还没有初始化git仓库
git init

# 添加所有文件
git add .

# 提交代码
git commit -m "Initial commit: 乡村公益平台完整版"

# 添加远程仓库（替换为你的GitHub用户名）
git remote add origin https://github.com/YOUR_USERNAME/rural-charity-platform.git

# 推送到GitHub
git push -u origin main
```

### 3. 启用GitHub Pages

1. 进入你的GitHub仓库页面
2. 点击 "Settings" 标签页
3. 在左侧菜单中找到 "Pages"
4. 在 "Source" 部分选择 "GitHub Actions"
5. 系统会自动检测到 `.github/workflows/deploy.yml` 文件

### 4. 等待部署完成

1. 推送代码后，GitHub Actions 会自动开始部署
2. 在仓库的 "Actions" 标签页可以查看部署进度
3. 部署成功后，你的网站将在以下地址可用：
   ```
   https://YOUR_USERNAME.github.io/rural-charity-platform/
   ```

## 🔧 配置说明

### 自动部署配置

项目已包含以下配置文件：

- `.github/workflows/deploy.yml` - GitHub Actions 自动部署配置
- `.nojekyll` - 禁用Jekyll处理，确保所有文件正常访问
- `CNAME` - 自定义域名配置（可选）

### 自定义域名（可选）

如果你有自己的域名：

1. 编辑 `CNAME` 文件，将内容替换为你的域名：
   ```
   your-domain.com
   ```

2. 在你的域名DNS设置中添加CNAME记录：
   ```
   CNAME: your-domain.com -> YOUR_USERNAME.github.io
   ```

## 📱 访问页面

部署成功后，你可以访问以下页面：

- **首页**: `https://YOUR_USERNAME.github.io/rural-charity-platform/`
- **乡村公益平台**: `https://YOUR_USERNAME.github.io/rural-charity-platform/乡村公益平台完整版-新版.html`
- **批量下发工具**: `https://YOUR_USERNAME.github.io/rural-charity-platform/批量下发工具.html`
- **小程序体验**: `https://YOUR_USERNAME.github.io/rural-charity-platform/公益项目小程序体验.html`

## 🔄 更新部署

每次推送代码到 `main` 分支时，GitHub Actions 会自动重新部署：

```bash
# 修改文件后
git add .
git commit -m "更新功能描述"
git push origin main
```

## ⚠️ 注意事项

1. **文件名编码**: 项目中包含中文文件名，GitHub Pages 完全支持
2. **相对路径**: 所有链接使用相对路径，确保在GitHub Pages上正常工作
3. **HTTPS**: GitHub Pages 自动提供HTTPS支持
4. **缓存**: 更新后可能需要强制刷新浏览器缓存（Ctrl+F5）

## 🛠️ 故障排除

### 部署失败
- 检查 Actions 标签页的错误日志
- 确保所有文件都已正确提交
- 验证 `.github/workflows/deploy.yml` 文件格式正确

### 页面无法访问
- 确认 GitHub Pages 已启用
- 检查仓库是否为 Public
- 等待几分钟让DNS生效

### 中文文件名问题
- GitHub Pages 支持UTF-8编码的文件名
- 如果遇到问题，可以考虑将文件名改为英文

## 📞 技术支持

如果遇到问题：
1. 查看GitHub Pages [官方文档](https://docs.github.com/en/pages)
2. 检查GitHub Actions [运行日志](https://docs.github.com/en/actions)
3. 在项目仓库中创建Issue

---

🎉 **恭喜！你的乡村公益平台现在已经成功部署到GitHub Pages！**
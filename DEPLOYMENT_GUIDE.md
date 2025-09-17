# GitHub Pages 部署指南

## 快速部署步骤

### 1. 创建GitHub仓库
- 访问 https://github.com/new
- 仓库名：`natural-selection-simulation`
- 描述：`基于PhET的自然选择模拟器 - 生物学教育工具`
- 选择 Public
- 不要添加 README（我们已经有了）

### 2. 连接本地仓库
```bash
# 替换 YOUR_USERNAME 为你的GitHub用户名
git remote add origin https://github.com/YOUR_USERNAME/natural-selection-simulation.git
git branch -M main
git push -u origin main
```

### 3. 启用GitHub Pages
1. 进入仓库页面
2. 点击 "Settings" 标签
3. 在左侧菜单找到 "Pages"
4. 在 "Source" 下选择 "GitHub Actions"
5. 保存设置

### 4. 自动部署
- GitHub Actions 会自动运行部署工作流
- 部署完成后，网站将在以下地址可用：
  `https://YOUR_USERNAME.github.io/natural-selection-simulation`

## 验证部署

### 检查部署状态
1. 在仓库页面点击 "Actions" 标签
2. 查看 "Deploy to GitHub Pages" 工作流状态
3. 绿色勾号表示部署成功

### 测试网站
1. 访问你的网站URL
2. 测试模拟器的各项功能
3. 确保在不同设备上都能正常显示

## 故障排除

### 常见问题
1. **部署失败**：检查 GitHub Actions 日志
2. **网站无法访问**：确认 Pages 设置正确
3. **功能异常**：检查浏览器控制台错误

### 重新部署
如果需要重新部署：
```bash
git add .
git commit -m "Update simulation"
git push origin main
```

## 自定义域名（可选）
1. 在 Pages 设置中添加自定义域名
2. 配置 DNS 记录指向 GitHub Pages
3. 启用 HTTPS

## 项目结构
```
natural-selection-simulation/
├── .github/workflows/deploy.yml  # 自动部署配置
├── index.html                    # 主页面
├── README.md                     # 项目说明
└── .gitignore                    # Git忽略文件
```

部署完成后，你的自然选择模拟器就可以在全球范围内访问了！

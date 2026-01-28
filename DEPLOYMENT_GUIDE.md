# 部署指南 | Deployment Guide

## 📦 当前状态

✅ Git仓库已初始化
✅ 文件已提交（16个文件，包含index.html和所有音频）
✅ README.md已创建
✅ .gitignore已配置

---

## 🚀 第三步：创建GitHub仓库并推送代码

### 方法一：使用GitHub网页界面（推荐）

1. **访问GitHub创建仓库**
   - 打开浏览器访问：https://github.com/new
   - 登录你的GitHub账号（如果还没登录）

2. **填写仓库信息**
   - Repository name（仓库名称）：`vlts-v46-educational-system`（或你喜欢的名称）
   - Description（描述）：`Astronomical-themed English learning system with 10 modules`
   - 选择 **Public**（公开，这样Netlify可以访问）
   - ⚠️ **不要勾选** "Initialize this repository with a README"（我们已经有了）
   - 点击 **Create repository** 按钮

3. **推送现有代码**

   创建完成后，GitHub会显示推送代码的命令。在你的项目文件夹中运行：

   ```bash
   cd /e/icc_gv
   git branch -M main
   git remote add origin https://github.com/你的用户名/仓库名.git
   git push -u origin main
   ```

   **示例**（假设你的GitHub用户名是Halienzo，仓库名是vlts-v46-educational-system）：
   ```bash
   cd /e/icc_gv
   git branch -M main
   git remote add origin https://github.com/Halienzo/vlts-v46-educational-system.git
   git push -u origin main
   ```

   首次推送时，会弹出登录窗口，输入你的GitHub凭证即可。

---

## 🌐 第四步：在Netlify上部署

### 方法一：通过GitHub自动部署（推荐）

1. **访问Netlify**
   - 打开：https://app.netlify.com/
   - 使用GitHub账号登录（推荐）或注册新账号

2. **导入Git仓库**
   - 点击 **"Add new site"** → **"Import an existing project"**
   - 选择 **"Deploy with GitHub"**
   - 授权Netlify访问你的GitHub账号
   - 在仓库列表中找到 `vlts-v46-educational-system` 并点击

3. **配置部署设置**
   - **Branch to deploy**: `main`
   - **Build command**: 留空（静态HTML，无需构建）
   - **Publish directory**: 留空或填 `.`（当前目录）
   - 点击 **"Deploy site"** 按钮

4. **等待部署完成**
   - Netlify会自动开始部署，通常需要1-2分钟
   - 部署成功后，会显示一个随机生成的网址，类似：
     `https://random-name-12345.netlify.app`

5. **（可选）自定义域名**
   - 点击 **"Domain settings"**
   - 可以修改为自定义的子域名，如：`vlts-education.netlify.app`
   - 或绑定你自己的域名

---

### 方法二：通过拖拽上传（快速但不推荐）

1. **访问Netlify**
   - 打开：https://app.netlify.com/drop

2. **准备部署文件**
   - 将以下文件复制到一个新文件夹：
     - index.html
     - 所有.mp3文件
     - 所有.mid文件

3. **拖拽上传**
   - 将文件夹直接拖到网页的拖放区域
   - 等待上传和部署完成

⚠️ **注意**：此方法不支持自动更新，每次修改都需要重新上传。

---

## 🎯 第五步：访问你的网站

部署完成后，你会获得一个网址，类似：
- `https://vlts-education.netlify.app`
- `https://your-custom-name.netlify.app`

直接在浏览器中打开即可访问你的教育系统！

---

## 🔄 后续更新流程

当你修改了代码后，只需要：

```bash
cd /e/icc_gv
git add .
git commit -m "描述你的修改"
git push
```

Netlify会自动检测到推送并重新部署（通常30秒-1分钟完成）。

---

## ⚠️ 常见问题

### Q1: 推送到GitHub时提示认证失败？
**A**: 从2021年起，GitHub不再支持密码认证。你需要：
- 使用 **Personal Access Token**（个人访问令牌）
- 或安装 **GitHub Desktop** 图形化工具
- 或安装 **Git Credential Manager**

**快速解决**：
1. 访问：https://github.com/settings/tokens
2. 点击 **"Generate new token (classic)"**
3. 勾选 `repo` 权限
4. 复制生成的token
5. 推送时用token代替密码

### Q2: Netlify部署失败？
**A**: 检查以下几点：
- 确保仓库是Public（公开）
- 确保index.html在根目录
- 检查浏览器控制台是否有错误

### Q3: 音频文件无法播放？
**A**: 检查：
- 音频文件是否都已推送到GitHub（`git status`检查）
- 浏览器控制台是否显示404错误
- HTML中的音频路径是否正确（应该是相对路径，如 `Cornfield Chase.mp3`）

### Q4: 页面加载很慢？
**A**: 音频文件总计约60MB，首次加载会比较慢。可以考虑：
- 使用CDN托管音频文件
- 压缩音频文件质量
- 实现懒加载（按需加载音频）

---

## 📞 需要帮助？

如果遇到问题，可以：
1. 查看Netlify的部署日志（Deploy log）
2. 检查GitHub仓库是否推送成功
3. 在浏览器中按F12查看控制台错误信息

---

**祝部署顺利！🎉**
